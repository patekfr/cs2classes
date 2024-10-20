```
#pragma once
#include <stdint.h>

using int8 = int8_t;
using uint8 = uint8_t;
using int16 = int16_t;
using uint16 = uint16_t;
using int32 = int32_t;
using uint32 = uint32_t;
using int64 = int64_t;
using uint64 = uint64_t;
using float32 = float;

struct vec3
{
    float x{}, y{}, z{};
};

struct color
{
    uint8_t m_r{}, m_g{}, m_b{}, m_a{};
};

using Color = color;
using Vector = vec3;
using QAngle = vec3;

struct  CScriptComponent {
    char m_pad[48];
};

struct __declspec(align(8)) C_BaseEntity {
    char m_pad[56];
    CBodyComponent* m_CBodyComponent; // Size: 8
    char m_NetworkTransmitComponent[736];
    void* m_nLastThinkTick;
    CGameSceneNode* m_pGameSceneNode; // Size: 8
    CRenderComponent* m_pRenderComponent; // Size: 8
    CCollisionProperty* m_pCollision; // Size: 8
    int32 m_iMaxHealth; // Size: 4
    int32 m_iHealth; // Size: 4
    uint8 m_lifeState; // Size: 1
    bool m_bTakesDamage; // Size: 7
    char m_pad6_848[6];
    void* m_nTakeDamageFlags;
    char m_nPlatformType[1];
    uint8 m_ubInterpolationFrame; // Size: 3
    char m_pad2_860[2];
    char m_hSceneObjectController[4];
    int32 m_nNoInterpolationTick; // Size: 4
    int32 m_nVisibilityNoInterpolationTick; // Size: 4
    float32 m_flProxyRandomValue; // Size: 4
    int32 m_iEFlags; // Size: 4
    uint8 m_nWaterType; // Size: 1
    bool m_bInterpolateEvenWithNoModel; // Size: 1
    bool m_bPredictionEligible; // Size: 1
    bool m_bApplyLayerMatchIDToModel; // Size: 1
    char m_tokLayerMatchID[4];
    char m_nSubclassID[16];
    int32 m_nSimulationTick; // Size: 4
    int32 m_iCurrentThinkContext; // Size: 4
    char m_aThinkFunctions[24];
    bool m_bDisabledContextThinks; // Size: 4
    char m_pad3_940[3];
    float32 m_flAnimTime; // Size: 4
    float32 m_flSimulationTime; // Size: 4
    uint8 m_nSceneObjectOverrideFlags; // Size: 1
    bool m_bHasSuccessfullyInterpolated; // Size: 1
    bool m_bHasAddedVarsToInterpolation; // Size: 1
    bool m_bRenderEvenWhenNotSuccessfullyInterpolated; // Size: 1
    void* m_nInterpolationLatchDirtyFlags;
    char m_ListEntry[24];
    char m_flCreateTime[4];
    float32 m_flSpeed; // Size: 4
    uint16 m_EntClientFlags; // Size: 2
    bool m_bClientSideRagdoll; // Size: 1
    uint8 m_iTeamNum; // Size: 1
    uint32 m_spawnflags; // Size: 4
    char m_nNextThinkTick[4];
    uint32 m_fFlags; // Size: 4
    Vector m_vecAbsVelocity; // Size: 16
    char m_vecVelocity[48];
    Vector m_vecBaseVelocity; // Size: 12
    char m_hEffectEntity[4];
    char m_hOwnerEntity[4];
    char m_MoveCollide[1];
    char m_MoveType[1];
    char m_nActualMoveType[2];
    float32 m_flWaterLevel; // Size: 4
    uint32 m_fEffects; // Size: 4
    char m_hGroundEntity[4];
    int32 m_nGroundBodyIndex; // Size: 4
    float32 m_flFriction; // Size: 4
    float32 m_flElasticity; // Size: 4
    float32 m_flGravityScale; // Size: 4
    float32 m_flTimeScale; // Size: 4
    bool m_bAnimatedEveryTick; // Size: 4
    char m_pad3_1132[3];
    char m_flNavIgnoreUntilTime[4];
    uint16 m_hThink; // Size: 16
    char m_pad14_1152[14];
    uint8 m_fBBoxVisFlags; // Size: 1
    bool m_bPredictable; // Size: 1
    bool m_bRenderWithViewModels; // Size: 2
    char m_pad1_1156[1];
    char m_nSplitUserPlayerPredictionSlot[4];
    int32 m_nFirstPredictableCommand; // Size: 4
    int32 m_nLastPredictableCommand; // Size: 4
    void* m_hOldMoveParent;
    char m_Particles[40];
    char m_vecPredictedScriptFloats[24];
    char m_vecPredictedScriptFloatIDs[48];
    int32 m_nNextScriptVarRecordID; // Size: 16
    char m_pad12_1304[12];
    QAngle m_vecAngVelocity; // Size: 12
    int32 m_DataChangeEventRef; // Size: 4
    char m_dependencies[24];
    int32 m_nCreationTick; // Size: 13
    char m_pad9_1357[9];
    bool m_bAnimTimeChanged; // Size: 1
    bool m_bSimulationTimeChanged; // Size: 10
    char m_pad9_1368[9];
    void* m_sUniqueHammerID;
};

struct  CountdownTimer {
    char m_pad[8];
    float32 m_duration; // Size: 4
    char m_timestamp[4];
    float32 m_timescale; // Size: 4
};

struct  CEntityComponent {
};

struct  CEntityIdentity {
    char m_pad[20];
    int32 m_nameStringableIndex; // Size: 4
    void* m_name;
    char m_designerName[16];
    uint32 m_flags; // Size: 8
    char m_pad4_56[4];
    char m_worldGroupId[4];
    uint32 m_fDataObjectTypes; // Size: 4
    char m_PathIndex[24];
    CEntityIdentity* m_pPrev; // Size: 8
    CEntityIdentity* m_pNext; // Size: 8
    CEntityIdentity* m_pPrevByClass; // Size: 8
};

struct  CEntityInstance {
    char m_pad[8];
    void* m_iszPrivateVScripts;
    CEntityIdentity* m_pEntity; // Size: 24
    CScriptComponent* m_CScriptComponent; // Size: 8
};

struct  CGameSceneNode {
    char m_pad[16];
    char m_nodeToWorld[32];
    CEntityInstance* m_pOwner; // Size: 8
    CGameSceneNode* m_pParent; // Size: 8
    CGameSceneNode* m_pChild; // Size: 8
    CGameSceneNode* m_pNextSibling; // Size: 48
    CGameSceneNodeHandle m_hParent; // Size: 16
    char m_vecOrigin[56];
    QAngle m_angRotation; // Size: 12
    float32 m_flScale; // Size: 4
    Vector m_vecAbsOrigin; // Size: 12
    QAngle m_angAbsRotation; // Size: 12
    float32 m_flAbsScale; // Size: 4
    int16 m_nParentAttachmentOrBone; // Size: 2
    bool m_bDebugAbsOriginChanges; // Size: 1
    bool m_bDormant; // Size: 1
    char m_bDirtyBoneMergeBoneToRoot[243];
    uint8 m_nHierarchicalDepth; // Size: 1
    uint8 m_nHierarchyType; // Size: 1
    uint8 m_nDoNotSetAnimTimeInInvalidatePhysicsCount; // Size: 3
    char m_pad2_248[2];
    char m_name[64];
    char m_hierarchyAttachName[4];
    float32 m_flZOffset; // Size: 4
    float32 m_flClientLocalScale; // Size: 4
};

struct  CBodyComponent {
    char m_pad[8];
    CGameSceneNode* m_pSceneNode; // Size: 24
};

struct  CBodyComponentPoint {
    char m_pad[80];
};

struct  CSkeletonInstance {
    char m_pad[368];
    CModelState m_modelState; // Size: 560
    bool m_bIsAnimationEnabled; // Size: 1
    bool m_bUseParentRenderBounds; // Size: 1
    char m_bIsGeneratingLatchedParentSpaceState[932];
    char m_materialGroup[4];
};

struct  CBodyComponentSkeletonInstance {
    char m_pad[80];
};

struct  CHitboxComponent {
    char m_pad[36];
};

struct  CLightComponent {
    char m_pad[56];
    char __m_pChainEntity[61];
    Color m_Color; // Size: 4
    Color m_SecondaryColor; // Size: 7
    float32 m_flBrightness; // Size: 4
    float32 m_flBrightnessScale; // Size: 4
    float32 m_flBrightnessMult; // Size: 4
    float32 m_flRange; // Size: 4
    float32 m_flFalloff; // Size: 4
    float32 m_flAttenuation0; // Size: 4
    float32 m_flAttenuation1; // Size: 4
    float32 m_flAttenuation2; // Size: 4
    float32 m_flTheta; // Size: 4
    float32 m_flPhi; // Size: 4
    void* m_hLightCookie;
    int32 m_nCascades; // Size: 4
    int32 m_nCastShadows; // Size: 4
    int32 m_nShadowWidth; // Size: 4
    int32 m_nShadowHeight; // Size: 4
    bool m_bRenderDiffuse; // Size: 4
    char m_pad3_196[3];
    int32 m_nRenderSpecular; // Size: 4
    bool m_bRenderTransmissive; // Size: 4
    char m_pad3_204[3];
    float32 m_flOrthoLightWidth; // Size: 4
    float32 m_flOrthoLightHeight; // Size: 4
    int32 m_nStyle; // Size: 4
    void* m_Pattern;
    int32 m_nCascadeRenderStaticObjects; // Size: 4
    float32 m_flShadowCascadeCrossFade; // Size: 4
    float32 m_flShadowCascadeDistanceFade; // Size: 4
    float32 m_flShadowCascadeDistance0; // Size: 4
    float32 m_flShadowCascadeDistance1; // Size: 4
    float32 m_flShadowCascadeDistance2; // Size: 4
    float32 m_flShadowCascadeDistance3; // Size: 4
    int32 m_nShadowCascadeResolution0; // Size: 4
    int32 m_nShadowCascadeResolution1; // Size: 4
    int32 m_nShadowCascadeResolution2; // Size: 4
    int32 m_nShadowCascadeResolution3; // Size: 4
    bool m_bUsesBakedShadowing; // Size: 4
    char m_pad3_272[3];
    int32 m_nShadowPriority; // Size: 4
    int32 m_nBakedShadowIndex; // Size: 4
    bool m_bRenderToCubemaps; // Size: 4
    char m_pad3_284[3];
    int32 m_nDirectLight; // Size: 4
    int32 m_nIndirectLight; // Size: 4
    float32 m_flFadeMinDist; // Size: 4
    float32 m_flFadeMaxDist; // Size: 4
    float32 m_flShadowFadeMinDist; // Size: 4
    float32 m_flShadowFadeMaxDist; // Size: 4
    bool m_bEnabled; // Size: 1
    bool m_bFlicker; // Size: 1
    bool m_bPrecomputedFieldsValid; // Size: 2
    char m_pad1_312[1];
    Vector m_vPrecomputedBoundsMins; // Size: 12
    Vector m_vPrecomputedBoundsMaxs; // Size: 12
    Vector m_vPrecomputedOBBOrigin; // Size: 12
    QAngle m_vPrecomputedOBBAngles; // Size: 12
    Vector m_vPrecomputedOBBExtent; // Size: 12
    float32 m_flPrecomputedMaxRange; // Size: 4
    int32 m_nFogLightingMode; // Size: 4
    float32 m_flFogContributionStength; // Size: 4
    float32 m_flNearClipPlane; // Size: 4
    Color m_SkyColor; // Size: 4
    float32 m_flSkyIntensity; // Size: 4
    Color m_SkyAmbientBounce; // Size: 4
    bool m_bUseSecondaryColor; // Size: 1
    bool m_bMixedShadows; // Size: 3
    char m_pad2_404[2];
    char m_flLightStyleStartTime[4];
    float32 m_flCapsuleLength; // Size: 4
};

struct  CRenderComponent {
    char m_pad[16];
    char __m_pChainEntity[64];
    bool m_bIsRenderingWithViewModels; // Size: 4
    char m_pad3_84[3];
    uint32 m_nSplitscreenFlags; // Size: 12
    char m_pad8_96[8];
    bool m_bEnableRendering; // Size: 80
    char m_pad79_176[79];
};

struct __declspec(align(8)) C_PointCamera {
    char m_pad[1384];
    float32 m_FOV; // Size: 4
    float32 m_Resolution; // Size: 4
    bool m_bFogEnable; // Size: 1
    Color m_FogColor; // Size: 7
    float32 m_flFogStart; // Size: 4
    float32 m_flFogEnd; // Size: 4
    float32 m_flFogMaxDensity; // Size: 4
    bool m_bActive; // Size: 1
    bool m_bUseScreenAspectRatio; // Size: 3
    char m_pad2_1416[2];
    float32 m_flAspectRatio; // Size: 4
    bool m_bNoSky; // Size: 4
    char m_pad3_1424[3];
    float32 m_fBrightness; // Size: 4
    float32 m_flZFar; // Size: 4
    float32 m_flZNear; // Size: 4
    bool m_bCanHLTVUse; // Size: 1
    bool m_bAlignWithParent; // Size: 1
    bool m_bDofEnabled; // Size: 2
    char m_pad1_1440[1];
    float32 m_flDofNearBlurry; // Size: 4
    float32 m_flDofNearCrisp; // Size: 4
    float32 m_flDofFarCrisp; // Size: 4
    float32 m_flDofFarBlurry; // Size: 4
    float32 m_flDofTiltToGround; // Size: 4
    float32 m_TargetFOV; // Size: 4
    float32 m_DegreesPerSecond; // Size: 4
    bool m_bIsOn; // Size: 4
    char m_pad3_1472[3];
};

struct  CPointTemplateAPI {
};

struct  CPropDataComponent {
    char m_pad[16];
    float32 m_flDmgModBullet; // Size: 4
    float32 m_flDmgModClub; // Size: 4
    float32 m_flDmgModExplosive; // Size: 4
    float32 m_flDmgModFire; // Size: 4
    void* m_iszPhysicsDamageTableName;
    void* m_iszBasePropData;
    int32 m_nInteractions; // Size: 4
    bool m_bSpawnMotionDisabled; // Size: 4
    char m_pad3_56[3];
    int32 m_nDisableTakePhysicsDamageSpawnFlag; // Size: 4
};

struct  CBuoyancyHelper {
    char m_pad[24];
    char m_nFluidType[4];
    float32 m_flFluidDensity; // Size: 4
    char m_vecFractionOfWheelSubmergedForWheelFriction[24];
    char m_vecWheelFrictionScales[24];
    char m_vecFractionOfWheelSubmergedForWheelDrag[24];
};

struct __declspec(align(8)) CBaseAnimGraph {
    char m_pad[3488];
    bool m_bInitiallyPopulateInterpHistory; // Size: 2
    char m_pad1_3490[1];
    bool m_bSuppressAnimEventSounds; // Size: 14
    char m_pad13_3504[13];
    bool m_bAnimGraphUpdateEnabled; // Size: 4
    char m_pad3_3508[3];
    float32 m_flMaxSlopeDistance; // Size: 4
    Vector m_vLastSlopeCheckPos; // Size: 12
    bool m_bAnimationUpdateScheduled; // Size: 4
    char m_pad3_3528[3];
    Vector m_vecForce; // Size: 12
    int32 m_nForceBone; // Size: 4
    CBaseAnimGraph* m_pClientsideRagdoll; // Size: 8
    bool m_bBuiltRagdoll; // Size: 24
    char m_pad23_3576[23];
    PhysicsRagdollPose_t m_RagdollPose; // Size: 72
    bool m_bRagdollClientSide; // Size: 16
    char m_pad15_3664[15];
};

struct  CSharedGapTypeQueryRegistration {
};

struct  CBasePlayerControllerAPI {
};

struct  C_CommandContext {
    bool needsprocessing; // Size: 160
    char m_pad159_160[159];
    char m_pad[160];
};

struct  ViewAngleServerChange_t {
    char m_pad[48];
    char nType[4];
    QAngle qAngle; // Size: 12
};

struct  CPlayer_AutoaimServices {
};

struct  audioparams_t {
    char m_pad[8];
    char localSound[96];
    int32 soundscapeIndex; // Size: 4
    uint8 localBits; // Size: 4
    char m_pad3_112[3];
    int32 soundscapeEntityListIndex; // Size: 4
};

struct  C_fogplayerparams_t {
    char m_pad[8];
    char m_hCtrl[4];
    float32 m_flTransitionTime; // Size: 4
    Color m_OldColor; // Size: 4
    float32 m_flOldStart; // Size: 4
    float32 m_flOldEnd; // Size: 4
    float32 m_flOldMaxDensity; // Size: 4
    float32 m_flOldHDRColorScale; // Size: 4
    float32 m_flOldFarZ; // Size: 4
    Color m_NewColor; // Size: 4
    float32 m_flNewStart; // Size: 4
    float32 m_flNewEnd; // Size: 4
    float32 m_flNewMaxDensity; // Size: 4
    float32 m_flNewHDRColorScale; // Size: 4
};

struct __declspec(align(8)) C_ColorCorrection {
    char m_pad[1384];
    Vector m_vecOrigin; // Size: 12
    float32 m_MinFalloff; // Size: 4
    float32 m_MaxFalloff; // Size: 4
    float32 m_flFadeInDuration; // Size: 4
    float32 m_flFadeOutDuration; // Size: 4
    float32 m_flMaxWeight; // Size: 4
    float32 m_flCurWeight; // Size: 4
    char m_netlookupFilename[512];
    bool m_bEnabled; // Size: 1
    bool m_bMaster; // Size: 1
    bool m_bClientSide; // Size: 1
    bool m_bExclusive; // Size: 1
    char m_bEnabledOnClient[4];
    char m_flCurWeightOnClient[4];
    char m_bFadingIn[4];
    char m_flFadeStartWeight[4];
    char m_flFadeStartTime[4];
};

struct __declspec(align(8)) C_TonemapController2 {
    char m_pad[1384];
    float32 m_flAutoExposureMin; // Size: 4
    float32 m_flAutoExposureMax; // Size: 4
    float32 m_flTonemapPercentTarget; // Size: 4
    float32 m_flTonemapPercentBrightPixels; // Size: 4
    float32 m_flTonemapMinAvgLum; // Size: 4
    float32 m_flExposureAdaptationSpeedUp; // Size: 4
    float32 m_flExposureAdaptationSpeedDown; // Size: 4
};

struct __declspec(align(8)) C_PostProcessingVolume {
    char m_pad[3392];
    void* m_hPostSettings;
    float32 m_flFadeDuration; // Size: 4
    float32 m_flMinLogExposure; // Size: 4
    float32 m_flMaxLogExposure; // Size: 4
    float32 m_flMinExposure; // Size: 4
    float32 m_flMaxExposure; // Size: 4
    float32 m_flExposureCompensation; // Size: 4
    float32 m_flExposureFadeSpeedUp; // Size: 4
    float32 m_flExposureFadeSpeedDown; // Size: 4
    float32 m_flTonemapEVSmoothingRange; // Size: 4
    bool m_bMaster; // Size: 1
    bool m_bExposureControl; // Size: 3
    char m_pad2_3440[2];
    float32 m_flRate; // Size: 4
    float32 m_flTonemapPercentTarget; // Size: 4
    float32 m_flTonemapPercentBrightPixels; // Size: 4
};

struct  fogparams_t {
    char m_pad[8];
    Vector dirPrimary; // Size: 12
    Color colorPrimary; // Size: 4
    Color colorSecondary; // Size: 4
    Color colorPrimaryLerpTo; // Size: 4
    Color colorSecondaryLerpTo; // Size: 4
    float32 start; // Size: 4
    float32 end; // Size: 4
    float32 farz; // Size: 4
    float32 maxdensity; // Size: 4
    float32 exponent; // Size: 4
    float32 HDRColorScale; // Size: 4
    float32 skyboxFogFactor; // Size: 4
    float32 skyboxFogFactorLerpTo; // Size: 4
    float32 startLerpTo; // Size: 4
    float32 endLerpTo; // Size: 4
    float32 maxdensityLerpTo; // Size: 4
    char lerptime[4];
    float32 duration; // Size: 4
    float32 blendtobackground; // Size: 4
    float32 scattering; // Size: 4
    float32 locallightscale; // Size: 4
    bool enable; // Size: 1
    bool blend; // Size: 1
    bool m_bNoReflectionFog; // Size: 1
};

struct __declspec(align(8)) C_FogController {
    char m_pad[1384];
    fogparams_t m_fog; // Size: 104
    bool m_bUseAngles; // Size: 4
    char m_pad3_1492[3];
};

struct  CPlayer_CameraServices {
    char m_pad[64];
    QAngle m_vecCsViewPunchAngle; // Size: 12
    char m_nCsViewPunchAngleTick[4];
    float32 m_flCsViewPunchAngleTickRatio; // Size: 8
    char m_pad4_88[4];
    C_fogplayerparams_t m_PlayerFog; // Size: 64
    char m_hColorCorrectionCtrl[4];
    char m_hViewEntity[4];
    void* m_hTonemapController;
    audioparams_t m_audio; // Size: 120
    char m_PostProcessingVolumes[24];
    float32 m_flOldPlayerZ; // Size: 4
    float32 m_flOldPlayerViewOffsetZ; // Size: 4
    fogparams_t m_CurrentFog; // Size: 104
    char m_hOldFogController[4];
    char m_bOverrideFogColor[5];
    char m_OverrideFogColor[20];
    char m_bOverrideFogStartEnd[7];
    char m_fOverrideFogStart[20];
    char m_fOverrideFogEnd[20];
    char m_hActivePostProcessingVolume[4];
};

struct  CPlayer_FlashlightServices {
};

struct  CPlayer_ItemServices {
};

struct  CPlayer_MovementServices {
    char m_pad[64];
    int32 m_nImpulse; // Size: 8
    char m_pad4_72[4];
    char m_nButtons[32];
    uint64 m_nQueuedButtonDownMask; // Size: 8
    uint64 m_nQueuedButtonChangeMask; // Size: 8
    uint64 m_nButtonDoublePressed; // Size: 8
    char m_pButtonPressedCmdNumber[256];
    uint32 m_nLastCommandNumberProcessed; // Size: 8
    char m_pad4_392[4];
    uint64 m_nToggleButtonDownMask; // Size: 16
    char m_pad8_408[8];
    float32 m_flMaxspeed; // Size: 4
    char m_arrForceSubtickMoveWhen[16];
    float32 m_flForwardMove; // Size: 4
    float32 m_flLeftMove; // Size: 4
    float32 m_flUpMove; // Size: 4
    Vector m_vecLastMovementImpulses; // Size: 12
};

struct  CPlayer_MovementServices_Humanoid {
    char m_pad[472];
    float32 m_flStepSoundTime; // Size: 4
    float32 m_flFallVelocity; // Size: 4
    bool m_bInCrouch; // Size: 4
    char m_pad3_484[3];
    uint32 m_nCrouchState; // Size: 4
    char m_flCrouchTransitionStartTime[4];
    bool m_bDucked; // Size: 1
    bool m_bDucking; // Size: 1
    bool m_bInDuckJump; // Size: 2
    char m_pad1_496[1];
    Vector m_groundNormal; // Size: 12
    float32 m_flSurfaceFriction; // Size: 4
    char m_surfaceProps[16];
};

struct  CPlayer_ObserverServices {
    char m_pad[64];
    uint8 m_iObserverMode; // Size: 4
    char m_pad3_68[3];
    char m_hObserverTarget[4];
    char m_iObserverLastMode[4];
    bool m_bForcedObserverMode; // Size: 4
    char m_pad3_80[3];
    float32 m_flObserverChaseDistance; // Size: 4
};

struct  CPlayer_UseServices {
};

struct  CPlayer_WaterServices {
};

struct __declspec(align(8)) C_BasePlayerWeapon {
    char m_pad[5736];
    char m_nNextPrimaryAttackTick[4];
    float32 m_flNextPrimaryAttackTickRatio; // Size: 4
    char m_nNextSecondaryAttackTick[4];
    float32 m_flNextSecondaryAttackTickRatio; // Size: 4
    int32 m_iClip1; // Size: 4
    int32 m_iClip2; // Size: 4
};

struct  CPlayer_WeaponServices {
    char m_pad[64];
    char m_hMyWeapons[24];
    char m_hActiveWeapon[4];
    char m_hLastWeapon[4];
};

struct  CBaseAnimGraphController {
    char m_pad[24];
    CAnimGraphNetworkedVariables m_animGraphNetworkedVars; // Size: 5264
    bool m_bSequenceFinished; // Size: 4
    char m_pad3_5292[3];
    float32 m_flSoundSyncTime; // Size: 4
    uint32 m_nActiveIKChainMask; // Size: 4
    char m_hSequence[4];
    char m_flSeqStartTime[4];
    float32 m_flSeqFixedCycle; // Size: 4
    char m_nAnimLoopMode[4];
    char m_flPlaybackRate[12];
    char m_nNotifyState[2];
    bool m_bNetworkedAnimationInputsChanged; // Size: 1
    bool m_bNetworkedSequenceChanged; // Size: 1
    bool m_bLastUpdateSkipped; // Size: 4
    char m_pad3_5336[3];
};

struct  CBodyComponentBaseAnimGraph {
    char m_pad[1168];
};

struct  EntityRenderAttribute_t {
    char m_pad[48];
    char m_ID[4];
};

struct __declspec(align(8)) C_BaseModelEntity {
    char m_pad[2640];
    CRenderComponent* m_CRenderComponent; // Size: 8
    CHitboxComponent m_CHitboxComponent; // Size: 40
    char m_LastHitGroup[40];
    bool m_bInitModelEffects; // Size: 1
    bool m_bIsStaticProp; // Size: 3
    char m_pad2_2732[2];
    int32 m_nLastAddDecal; // Size: 4
    int32 m_nDecalsAdded; // Size: 4
    int32 m_iOldHealth; // Size: 4
    char m_nRenderMode[1];
    char m_nRenderFX[1];
    bool m_bAllowFadeInView; // Size: 30
    char m_pad29_2776[29];
    Color m_clrRender; // Size: 8
    char m_vecRenderAttributes[104];
    bool m_bRenderToCubemaps; // Size: 1
    bool m_bNoInterpolate; // Size: 7
    char m_pad6_2896[6];
    CCollisionProperty m_Collision; // Size: 176
    CGlowProperty m_Glow; // Size: 88
    float32 m_flGlowBackfaceMult; // Size: 4
    float32 m_fadeMinDist; // Size: 4
    float32 m_fadeMaxDist; // Size: 4
    float32 m_flFadeScale; // Size: 4
    float32 m_flShadowStrength; // Size: 4
    uint8 m_nObjectCulling; // Size: 4
    char m_pad3_3184[3];
    int32 m_nAddDecal; // Size: 4
    Vector m_vDecalPosition; // Size: 12
    Vector m_vDecalForwardAxis; // Size: 12
    float32 m_flDecalHealBloodRate; // Size: 4
    float32 m_flDecalHealHeightRate; // Size: 8
    char m_pad4_3224[4];
    char m_ConfigEntitiesToPropagateMaterialDecalsTo[24];
    char m_vecViewOffset[48];
    CClientAlphaProperty* m_pClientAlphaProperty; // Size: 8
    Color m_ClientOverrideTint; // Size: 4
};

struct  ActiveModelConfig_t {
    char m_pad[40];
    void* m_Handle;
    void* m_Name;
    char m_AssociatedEntities[24];
};

struct  CBodyComponentBaseModelEntity {
};

struct  CGameSceneNodeHandle {
    char m_pad[8];
    char m_hOwner[4];
};

struct  CPathSimpleAPI {
};

struct  SequenceHistory_t {
    char m_hSequence[4];
    char m_pad[4];
    char m_flSeqStartTime[4];
    float32 m_flSeqFixedCycle; // Size: 4
    char m_nSeqLoopMode[4];
    float32 m_flPlaybackRate; // Size: 4
};

struct  CNetworkedSequenceOperation {
    char m_pad[8];
    char m_hSequence[4];
    float32 m_flPrevCycle; // Size: 4
    float32 m_flCycle; // Size: 4
    void* m_flWeight;
    bool m_bSequenceChangeNetworked; // Size: 1
    bool m_bDiscontinuity; // Size: 3
    char m_pad2_32[2];
    float32 m_flPrevCycleFromDiscontinuity; // Size: 4
};

struct  CModelState {
    char m_pad[160];
    void* m_hModel;
    char m_ModelName[64];
    bool m_bClientClothCreationSuppressed; // Size: 176
    char m_pad175_408[175];
    uint64 m_MeshGroupMask; // Size: 130
    char m_pad122_538[122];
    int8 m_nIdealMotionType; // Size: 1
    int8 m_nForceLOD; // Size: 1
};

struct  IntervalTimer {
    char m_pad[8];
    char m_timestamp[4];
};

struct  EngineCountdownTimer {
    char m_pad[8];
    float32 m_duration; // Size: 4
    float32 m_timestamp; // Size: 4
};

struct  CTimeline {
    char m_pad[16];
    char m_flValues[256];
    char m_nValueCounts[256];
    int32 m_nBucketCount; // Size: 4
    float32 m_flInterval; // Size: 4
    float32 m_flFinalValue; // Size: 4
    char m_nCompressionType[4];
};

struct  CAnimGraphNetworkedVariables {
    char m_pad[8];
    char m_PredNetBoolVariables[24];
    char m_PredNetByteVariables[24];
    char m_PredNetUInt16Variables[24];
    char m_PredNetIntVariables[24];
    char m_PredNetUInt32Variables[24];
    char m_PredNetUInt64Variables[24];
    char m_PredNetFloatVariables[24];
    char m_PredNetVectorVariables[24];
    char m_PredNetQuaternionVariables[24];
    char m_PredNetGlobalSymbolVariables[24];
    char m_OwnerOnlyPredNetBoolVariables[24];
    char m_OwnerOnlyPredNetByteVariables[24];
    char m_OwnerOnlyPredNetUInt16Variables[24];
    char m_OwnerOnlyPredNetIntVariables[24];
    char m_OwnerOnlyPredNetUInt32Variables[24];
    char m_OwnerOnlyPredNetUInt64Variables[24];
    char m_OwnerOnlyPredNetFloatVariables[24];
    char m_OwnerOnlyPredNetVectorVariables[24];
    char m_OwnerOnlyPredNetQuaternionVariables[24];
    char m_OwnerOnlyPredNetGlobalSymbolVariables[24];
    int32 m_nBoolVariablesCount; // Size: 4
    int32 m_nOwnerOnlyBoolVariablesCount; // Size: 4
    int32 m_nRandomSeedOffset; // Size: 4
};

struct  C_BaseEntityAPI {
};

struct  CTakeDamageInfoAPI {
};

struct  CClientGapTypeQueryRegistration {
};

struct  CCollisionProperty {
    char m_pad[16];
    VPhysicsCollisionAttribute_t m_collisionAttribute; // Size: 48
    Vector m_vecMins; // Size: 12
    Vector m_vecMaxs; // Size: 14
    uint8 m_usSolidFlags; // Size: 1
    char m_nSolidType[1];
    uint8 m_triggerBloat; // Size: 1
    char m_nSurroundType[1];
    uint8 m_CollisionGroup; // Size: 1
    uint8 m_nEnablePhysics; // Size: 1
    float32 m_flBoundingRadius; // Size: 4
    Vector m_vecSpecifiedSurroundingMins; // Size: 12
    Vector m_vecSpecifiedSurroundingMaxs; // Size: 12
    Vector m_vecSurroundingMaxs; // Size: 12
    Vector m_vecSurroundingMins; // Size: 12
    Vector m_vCapsuleCenter1; // Size: 12
    Vector m_vCapsuleCenter2; // Size: 12
};

struct __declspec(align(8)) CBasePlayerController {
    char m_pad[1392];
    int32 m_nFinalPredictedTick; // Size: 8
    char m_pad4_1400[4];
    C_CommandContext m_CommandContext; // Size: 168
    uint64 m_nInButtonsWhichAreToggles; // Size: 8
    uint32 m_nTickBase; // Size: 4
    char m_hPawn[4];
    bool m_bKnownTeamMismatch; // Size: 4
    char m_pad3_1588[3];
    char m_hPredictedPawn[4];
    char m_nSplitScreenSlot[4];
    char m_hSplitOwner[4];
    char m_hSplitScreenPlayers[24];
    bool m_bIsHLTV; // Size: 4
    char m_pad3_1628[3];
    char m_iConnected[4];
    char m_iszPlayerName[136];
    uint64 m_steamID; // Size: 8
    bool m_bIsLocalPlayerController; // Size: 4
    char m_pad3_1780[3];
};

struct __declspec(align(8)) CLogicalEntity {
};

struct  C_BaseFlex__Emphasized_Phoneme {
    char m_sClassName[24];
    char m_pad[24];
    float32 m_flAmount; // Size: 4
    bool m_bRequired; // Size: 1
    bool m_bBasechecked; // Size: 1
};

struct  C_EnvWindShared {
    char m_pad[8];
    char m_flStartTime[4];
    uint32 m_iWindSeed; // Size: 4
    uint16 m_iMinWind; // Size: 2
    uint16 m_iMaxWind; // Size: 2
    int32 m_windRadius; // Size: 4
    uint16 m_iMinGust; // Size: 2
    uint16 m_iMaxGust; // Size: 2
    float32 m_flMinGustDelay; // Size: 4
    float32 m_flMaxGustDelay; // Size: 4
    float32 m_flGustDuration; // Size: 4
    uint16 m_iGustDirChange; // Size: 4
    char m_pad2_44[2];
    Vector m_location; // Size: 12
    int32 m_iszGustSound; // Size: 4
    int32 m_iWindDir; // Size: 4
    float32 m_flWindSpeed; // Size: 4
    Vector m_currentWindVector; // Size: 12
    Vector m_CurrentSwayVector; // Size: 12
    Vector m_PrevSwayVector; // Size: 12
    uint16 m_iInitialWindDir; // Size: 4
    char m_pad2_108[2];
    float32 m_flInitialWindSpeed; // Size: 4
    char m_flVariationTime[4];
    char m_flSwayTime[4];
    char m_flSimTime[4];
    char m_flSwitchTime[4];
    float32 m_flAveWindSpeed; // Size: 4
    bool m_bGusting; // Size: 4
    char m_pad3_136[3];
    float32 m_flWindAngleVariation; // Size: 4
    float32 m_flWindSpeedVariation; // Size: 4
};

struct __declspec(align(8)) C_EnvWindClientside {
    char m_pad[1384];
};

struct __declspec(align(8)) C_EntityFlame {
    char m_pad[1384];
    char m_hEntAttached[40];
    char m_hOldAttached[4];
};

struct  CProjectedTextureBase {
    char m_pad[12];
    char m_hTargetEntity[4];
    bool m_bState; // Size: 1
    bool m_bAlwaysUpdate; // Size: 3
    char m_pad2_20[2];
    float32 m_flLightFOV; // Size: 4
    bool m_bEnableShadows; // Size: 1
    bool m_bSimpleProjection; // Size: 1
    bool m_bLightOnlyTarget; // Size: 1
    bool m_bLightWorld; // Size: 1
    bool m_bCameraSpace; // Size: 4
    char m_pad3_32[3];
    float32 m_flBrightnessScale; // Size: 4
    Color m_LightColor; // Size: 4
    float32 m_flIntensity; // Size: 4
    float32 m_flLinearAttenuation; // Size: 4
    float32 m_flQuadraticAttenuation; // Size: 4
    bool m_bVolumetric; // Size: 4
    char m_pad3_56[3];
    float32 m_flVolumetricIntensity; // Size: 4
    float32 m_flNoiseStrength; // Size: 4
    float32 m_flFlashlightTime; // Size: 4
    uint32 m_nNumPlanes; // Size: 4
    float32 m_flPlaneOffset; // Size: 4
    float32 m_flColorTransitionTime; // Size: 4
    float32 m_flAmbient; // Size: 4
    char m_SpotlightTextureName[512];
    int32 m_nSpotlightTextureFrame; // Size: 4
    uint32 m_nShadowQuality; // Size: 4
    float32 m_flNearZ; // Size: 4
    float32 m_flFarZ; // Size: 4
    float32 m_flProjectionSize; // Size: 4
    float32 m_flRotation; // Size: 4
};

struct __declspec(align(8)) C_BaseFire {
    char m_pad[1384];
    float32 m_flScale; // Size: 4
    float32 m_flStartScale; // Size: 4
    float32 m_flScaleTime; // Size: 4
};

struct  TimedEvent {
    float32 m_TimeBetweenEvents; // Size: 4
    char m_pad[4];
};

struct  CFireOverlay {
    char m_pad[208];
    C_FireSmoke* m_pOwner; // Size: 8
    char m_vBaseColors[48];
    float32 m_flScale; // Size: 4
};

struct __declspec(align(8)) C_FireSmoke {
    char m_pad[1400];
    int32 m_nFlameModelIndex; // Size: 4
    int32 m_nFlameFromAboveModelIndex; // Size: 4
    float32 m_flScaleRegister; // Size: 4
    float32 m_flScaleStart; // Size: 4
    float32 m_flScaleEnd; // Size: 4
    char m_flScaleTimeStart[4];
    char m_flScaleTimeEnd[4];
    float32 m_flChildFlameSpread; // Size: 20
    char m_pad16_1448[16];
    float32 m_flClipPerc; // Size: 4
    bool m_bClipTested; // Size: 1
    bool m_bFadingOut; // Size: 3
    char m_pad2_1456[2];
    TimedEvent m_tParticleSpawn; // Size: 8
};

struct __declspec(align(8)) C_RopeKeyframe {
    char m_pad[3376];
    char m_LinksTouchingSomething[4];
    int32 m_nLinksTouchingSomething; // Size: 4
    bool m_bApplyWind; // Size: 4
    char m_pad3_3388[3];
    int32 m_fPrevLockedPoints; // Size: 4
    int32 m_iForcePointMoveCounter; // Size: 4
    char m_bPrevEndPointPos[4];
    char m_vPrevEndPointPos[24];
    float32 m_flCurScroll; // Size: 4
    float32 m_flScrollSpeed; // Size: 4
    uint16 m_RopeFlags; // Size: 8
    char m_pad6_3440[6];
    char m_iRopeMaterialModelIndex[632];
    char m_LightValues[120];
    uint8 m_nSegments; // Size: 4
    char m_pad3_4196[3];
    char m_hStartPoint[4];
    char m_hEndPoint[4];
    char m_iStartAttachment[1];
    char m_iEndAttachment[1];
    uint8 m_Subdiv; // Size: 2
    char m_pad1_4208[1];
    int16 m_RopeLength; // Size: 2
    int16 m_Slack; // Size: 2
    float32 m_TextureScale; // Size: 4
    uint8 m_fLockedPoints; // Size: 1
    uint8 m_nChangeCount; // Size: 3
    char m_pad2_4220[2];
    float32 m_Width; // Size: 4
    char m_PhysicsDelegate[16];
    void* m_hMaterial;
    int32 m_TextureHeight; // Size: 4
    Vector m_vecImpulse; // Size: 12
    Vector m_vecPreviousImpulse; // Size: 12
    float32 m_flCurrentGustTimer; // Size: 4
    float32 m_flCurrentGustLifetime; // Size: 4
    float32 m_flTimeToNextGust; // Size: 4
    Vector m_vWindDir; // Size: 12
    Vector m_vColorMod; // Size: 12
    char m_vCachedEndPointAttachmentPos[24];
    char m_vCachedEndPointAttachmentAngle[24];
};

struct  C_RopeKeyframe__CPhysicsDelegate {
    char m_pad[8];
};

struct  C_SceneEntity__QueuedEvents_t {
};

struct __declspec(align(8)) C_TintController {
};

struct  CFlashlightEffect {
    char m_pad[16];
    bool m_bIsOn; // Size: 16
    char m_pad15_32[15];
    bool m_bMuzzleFlashEnabled; // Size: 4
    char m_pad3_36[3];
    float32 m_flMuzzleFlashBrightness; // Size: 12
    char m_pad8_48[8];
    char m_quatMuzzleFlashOrientation[16];
    Vector m_vecMuzzleFlashOrigin; // Size: 12
    float32 m_flFov; // Size: 4
    float32 m_flFarZ; // Size: 4
    float32 m_flLinearAtten; // Size: 4
    bool m_bCastsShadows; // Size: 4
    char m_pad3_92[3];
    float32 m_flCurrentPullBackDist; // Size: 4
    void* m_FlashlightTexture;
    void* m_MuzzleFlashTexture;
};

struct  CInterpolatedValue {
    float32 m_flStartTime; // Size: 4
    char m_pad[4];
    float32 m_flEndTime; // Size: 4
    float32 m_flStartValue; // Size: 4
    float32 m_flEndValue; // Size: 4
};

struct  CGlowSprite {
    Vector m_vColor; // Size: 12
    char m_pad[12];
    float32 m_flHorzSize; // Size: 4
    float32 m_flVertSize; // Size: 8
    char m_pad4_24[4];
};

struct  CGlowOverlay {
    char m_pad[8];
    Vector m_vPos; // Size: 12
    bool m_bDirectional; // Size: 4
    char m_pad3_24[3];
    Vector m_vDirection; // Size: 12
    bool m_bInSky; // Size: 4
    char m_pad3_40[3];
    float32 m_skyObstructionScale; // Size: 8
    char m_pad4_48[4];
    char m_Sprites[128];
    int32 m_nSprites; // Size: 4
    float32 m_flProxyRadius; // Size: 4
    float32 m_flHDRColorScale; // Size: 4
    float32 m_flGlowObstructionScale; // Size: 4
    bool m_bCacheGlowObstruction; // Size: 1
    bool m_bCacheSkyObstruction; // Size: 1
    int16 m_bActivated; // Size: 2
    uint16 m_ListIndex; // Size: 4
    char m_pad2_200[2];
};

struct  IClientAlphaProperty {
};

struct __declspec(align(8)) C_SkyCamera {
    char m_pad[1384];
    sky3dparams_t m_skyboxData; // Size: 144
    char m_skyboxSlotToken[4];
    bool m_bUseAngles; // Size: 4
    char m_pad3_1536[3];
};

struct __declspec(align(8)) CSkyboxReference {
    char m_pad[1384];
    char m_worldGroupId[4];
};

struct  sky3dparams_t {
    char m_pad[8];
    int16 scale; // Size: 4
    char m_pad2_12[2];
    Vector origin; // Size: 12
    bool bClip3DSkyBoxNearToWorldFar; // Size: 4
    char m_pad3_28[3];
    float32 flClip3DSkyBoxNearToWorldFarOffset; // Size: 4
    fogparams_t fog; // Size: 104
};

struct  VPhysicsCollisionAttribute_t {
    char m_pad[8];
    uint64 m_nInteractsAs; // Size: 8
    uint64 m_nInteractsWith; // Size: 8
    uint64 m_nInteractsExclude; // Size: 8
    uint32 m_nEntityId; // Size: 4
    uint32 m_nOwnerId; // Size: 4
    uint16 m_nHierarchyId; // Size: 2
    uint8 m_nCollisionGroup; // Size: 1
};

struct  CDecalInfo {
    float32 m_flAnimationScale; // Size: 4
    char m_pad[4];
    float32 m_flAnimationLifeSpan; // Size: 4
    float32 m_flPlaceTime; // Size: 4
    float32 m_flFadeStartTime; // Size: 4
    float32 m_flFadeDuration; // Size: 4
    int32 m_nVBSlot; // Size: 4
    int32 m_nBoneIndex; // Size: 16
    char m_pad12_40[12];
    Vector m_vPosition; // Size: 12
    float32 m_flBoundingRadiusSqr; // Size: 12
    char m_pad8_64[8];
    CDecalInfo* m_pNext; // Size: 8
    CDecalInfo* m_pPrev; // Size: 136
};

struct  CEffectData {
    char m_pad[8];
    Vector m_vOrigin; // Size: 12
    Vector m_vStart; // Size: 12
    Vector m_vNormal; // Size: 12
    QAngle m_vAngles; // Size: 12
    char m_hEntity[4];
    char m_hOtherEntity[4];
    float32 m_flScale; // Size: 4
    float32 m_flMagnitude; // Size: 4
    float32 m_flRadius; // Size: 4
    char m_nSurfaceProp[4];
    void* m_nEffectIndex;
    uint32 m_nDamageType; // Size: 4
    uint8 m_nPenetrate; // Size: 2
    char m_pad1_94[1];
    uint16 m_nMaterial; // Size: 2
    uint16 m_nHitBox; // Size: 2
    uint8 m_nColor; // Size: 1
    uint8 m_fFlags; // Size: 1
    char m_nAttachmentIndex[4];
    char m_nAttachmentName[4];
    uint16 m_iEffectName; // Size: 2
};

struct __declspec(align(8)) C_EnvDetailController {
    char m_pad[1384];
    float32 m_flFadeStartDist; // Size: 4
};

struct  C_EnvWindShared__WindAveEvent_t {
    float32 m_flStartWindSpeed; // Size: 4
    char m_pad[4];
};

struct  C_EnvWindShared__WindVariationEvent_t {
    float32 m_flWindAngleVariation; // Size: 4
    char m_pad[4];
};

struct __declspec(align(8)) C_InfoLadderDismount {
};

struct  shard_model_desc_t {
    char m_pad[8];
    int32 m_nModelID; // Size: 8
    char m_pad4_16[4];
    void* m_hMaterialBase;
    void* m_hMaterialDamageOverlay;
    char m_solid[4];
    void* m_vecPanelSize;
    void* m_vecStressPositionA;
    char m_vecStressPositionB[12];
    char m_vecPanelVertices[24];
    char m_vInitialPanelVertices[24];
    float32 m_flGlassHalfThickness; // Size: 4
    bool m_bHasParent; // Size: 1
    bool m_bParentFrozen; // Size: 3
    char m_pad2_120[2];
};

struct __declspec(align(8)) C_GameRulesProxy {
};

struct  C_GameRules {
    char m_pad[8];
    char __m_pChainEntity[40];
    int32 m_nTotalPausedTicks; // Size: 4
    int32 m_nPauseStartTick; // Size: 4
};

struct  CGlowProperty {
    char m_pad[8];
    Vector m_fGlowColor; // Size: 40
    int32 m_iGlowType; // Size: 4
    int32 m_iGlowTeam; // Size: 4
    int32 m_nGlowRange; // Size: 4
    int32 m_nGlowRangeMin; // Size: 4
    Color m_glowColorOverride; // Size: 4
    bool m_bFlashing; // Size: 4
    char m_pad3_72[3];
    float32 m_flGlowTime; // Size: 4
    float32 m_flGlowStartTime; // Size: 4
    bool m_bEligibleForScreenHighlight; // Size: 1
};

struct  C_MultiplayRules {
};

struct __declspec(align(8)) PhysicsRagdollPose_t {
    char m_pad[8];
    char m_Transforms[24];
};

struct  C_SingleplayRules {
};

struct __declspec(align(8)) C_SoundOpvarSetPointBase {
    char m_pad[1384];
    void* m_iszStackName;
    void* m_iszOperatorName;
    void* m_iszOpvarName;
    int32 m_iOpvarIndex; // Size: 4
};

struct __declspec(align(8)) C_SoundOpvarSetPointEntity {
};

struct __declspec(align(8)) C_SoundOpvarSetAABBEntity {
};

struct __declspec(align(8)) C_SoundOpvarSetOBBEntity {
};

struct __declspec(align(8)) C_SoundOpvarSetPathCornerEntity {
};

struct __declspec(align(8)) C_SoundOpvarSetAutoRoomEntity {
};

struct __declspec(align(8)) C_SoundOpvarSetOBBWindEntity {
};

struct  C_TeamplayRules {
};

struct __declspec(align(8)) C_TeamRoundTimer {
    char m_pad[1384];
    bool m_bTimerPaused; // Size: 4
    char m_pad3_1388[3];
    float32 m_flTimeRemaining; // Size: 4
    char m_flTimerEndTime[4];
    bool m_bIsDisabled; // Size: 1
    bool m_bShowInHUD; // Size: 3
    char m_pad2_1400[2];
    int32 m_nTimerLength; // Size: 4
    int32 m_nTimerInitialLength; // Size: 4
    int32 m_nTimerMaxLength; // Size: 4
    bool m_bAutoCountdown; // Size: 4
    char m_pad3_1416[3];
    int32 m_nSetupTimeLength; // Size: 4
    int32 m_nState; // Size: 4
    bool m_bStartPaused; // Size: 1
    bool m_bInCaptureWatchState; // Size: 3
    char m_pad2_1428[2];
    float32 m_flTotalTime; // Size: 4
    bool m_bStopWatchTimer; // Size: 1
    bool m_bFireFinished; // Size: 1
    bool m_bFire5MinRemain; // Size: 1
    bool m_bFire4MinRemain; // Size: 1
    bool m_bFire3MinRemain; // Size: 1
    bool m_bFire2MinRemain; // Size: 1
    bool m_bFire1MinRemain; // Size: 1
    bool m_bFire30SecRemain; // Size: 1
    bool m_bFire10SecRemain; // Size: 1
    bool m_bFire5SecRemain; // Size: 1
    bool m_bFire4SecRemain; // Size: 1
    bool m_bFire3SecRemain; // Size: 1
    bool m_bFire2SecRemain; // Size: 1
    bool m_bFire1SecRemain; // Size: 3
    char m_pad2_1448[2];
    int32 m_nOldTimerLength; // Size: 4
};

struct __declspec(align(8)) C_PortraitWorldCallbackHandler {
};

struct  CEconItemAttribute {
    char m_pad[48];
    uint16 m_iAttributeDefinitionIndex; // Size: 4
    char m_pad2_52[2];
    float32 m_flValue; // Size: 4
    float32 m_flInitialValue; // Size: 4
    int32 m_nRefundableCurrency; // Size: 4
};

struct  CAttributeManager {
    char m_pad[8];
    char m_Providers[24];
    int32 m_iReapplyProvisionParity; // Size: 4
    char m_hOuter[4];
    bool m_bPreventLoopback; // Size: 4
    char m_pad3_44[3];
    char m_ProviderType[4];
};

struct  CAttributeList {
    char m_pad[8];
    char m_Attributes[80];
};

struct  CAttributeManager__cached_attribute_float_t {
    float32 flIn; // Size: 8
    char m_pad4_8[4];
    char m_pad[8];
    void* iAttribHook;
};

struct  C_EconItemView {
    char m_pad[96];
    bool m_bInventoryImageRgbaRequested; // Size: 1
    bool m_bInventoryImageTriedCache; // Size: 31
    char m_pad30_128[30];
    int32 m_nInventoryImageRgbaWidth; // Size: 4
    int32 m_nInventoryImageRgbaHeight; // Size: 4
    char m_szCurrentLoadCachedFileName[304];
    bool m_bRestoreCustomMaterialAfterPrecache; // Size: 2
    char m_pad1_442[1];
    uint16 m_iItemDefinitionIndex; // Size: 2
    int32 m_iEntityQuality; // Size: 4
    uint32 m_iEntityLevel; // Size: 8
    char m_pad4_456[4];
    uint64 m_iItemID; // Size: 8
    uint32 m_iItemIDHigh; // Size: 4
    uint32 m_iItemIDLow; // Size: 4
    uint32 m_iAccountID; // Size: 4
    uint32 m_iInventoryPosition; // Size: 12
    char m_pad8_488[8];
    bool m_bInitialized; // Size: 1
    bool m_bDisallowSOC; // Size: 1
    bool m_bIsStoreItem; // Size: 1
    bool m_bIsTradeItem; // Size: 1
    int32 m_iEntityQuantity; // Size: 4
    int32 m_iRarityOverride; // Size: 4
    int32 m_iQualityOverride; // Size: 4
    int32 m_iOriginOverride; // Size: 4
    uint8 m_unClientFlags; // Size: 1
    uint8 m_unOverrideStyle; // Size: 19
    char m_pad18_528[18];
    CAttributeList m_AttributeList; // Size: 96
    CAttributeList m_NetworkedDynamicAttributes; // Size: 96
    char m_szCustomName[161];
    char m_szCustomNameOverride[207];
};

struct  C_AttributeContainer {
    char m_pad[80];
    C_EconItemView m_Item; // Size: 1096
    int32 m_iExternalItemProviderRegisteredToken; // Size: 8
    char m_pad4_1184[4];
};

struct  C_EconEntity__AttachedModelData_t {
};

struct  EntitySpottedState_t {
    char m_pad[8];
    bool m_bSpotted; // Size: 4
    char m_pad3_12[3];
};

struct  C_CSGameRules {
    char m_pad[64];
    bool m_bFreezePeriod; // Size: 1
    bool m_bWarmupPeriod; // Size: 3
    char m_pad2_68[2];
    char m_fWarmupPeriodEnd[4];
    char m_fWarmupPeriodStart[4];
    bool m_bServerPaused; // Size: 1
    bool m_bTerroristTimeOutActive; // Size: 1
    bool m_bCTTimeOutActive; // Size: 2
    char m_pad1_80[1];
    float32 m_flTerroristTimeOutRemaining; // Size: 4
    float32 m_flCTTimeOutRemaining; // Size: 4
    int32 m_nTerroristTimeOuts; // Size: 4
    int32 m_nCTTimeOuts; // Size: 4
    bool m_bTechnicalTimeOut; // Size: 1
    bool m_bMatchWaitingForResume; // Size: 3
    char m_pad2_100[2];
    int32 m_iRoundTime; // Size: 4
    float32 m_fMatchStartTime; // Size: 4
    char m_fRoundStartTime[4];
    char m_flRestartRoundTime[4];
    bool m_bGameRestart; // Size: 4
    char m_pad3_120[3];
    float32 m_flGameStartTime; // Size: 4
    float32 m_timeUntilNextPhaseStarts; // Size: 4
    int32 m_gamePhase; // Size: 4
    int32 m_totalRoundsPlayed; // Size: 4
    int32 m_nRoundsPlayedThisPhase; // Size: 4
    int32 m_nOvertimePlaying; // Size: 4
    int32 m_iHostagesRemaining; // Size: 4
    bool m_bAnyHostageReached; // Size: 1
    bool m_bMapHasBombTarget; // Size: 1
    bool m_bMapHasRescueZone; // Size: 1
    bool m_bMapHasBuyZone; // Size: 1
    bool m_bIsQueuedMatchmaking; // Size: 4
    char m_pad3_156[3];
    int32 m_nQueuedMatchmakingMode; // Size: 4
    bool m_bIsValveDS; // Size: 1
    bool m_bLogoMap; // Size: 1
    bool m_bPlayAllStepSoundsOnServer; // Size: 2
    char m_pad1_164[1];
    int32 m_iSpectatorSlotCount; // Size: 4
    int32 m_MatchDevice; // Size: 4
    bool m_bHasMatchStarted; // Size: 4
    char m_pad3_176[3];
    int32 m_nNextMapInMapgroup; // Size: 4
    char m_szTournamentEventName[512];
    char m_szTournamentEventStage[512];
    char m_szMatchStatTxt[512];
    char m_szTournamentPredictionsTxt[512];
    int32 m_nTournamentPredictionsPct; // Size: 4
    char m_flCMMItemDropRevealStartTime[4];
    char m_flCMMItemDropRevealEndTime[4];
    bool m_bIsDroppingItems; // Size: 1
    bool m_bIsQuestEligible; // Size: 1
    bool m_bIsHltvActive; // Size: 2
    char m_pad1_2244[1];
    char m_arrProhibitedItemIndices[200];
    char m_arrTournamentActiveCasterAccounts[16];
    int32 m_numBestOfMaps; // Size: 4
    int32 m_nHalloweenMaskListSeed; // Size: 4
    bool m_bBombDropped; // Size: 1
    bool m_bBombPlanted; // Size: 3
    char m_pad2_2472[2];
    int32 m_iRoundWinStatus; // Size: 4
    int32 m_eRoundWinReason; // Size: 4
    bool m_bTCantBuy; // Size: 1
    bool m_bCTCantBuy; // Size: 3
    char m_pad2_2484[2];
    char m_iMatchStats_RoundResults[120];
    char m_iMatchStats_PlayersAlive_CT[120];
    char m_iMatchStats_PlayersAlive_T[120];
    char m_TeamRespawnWaveTimes[128];
    char m_flNextRespawnWave[128];
    int32 m_nServerQuestID; // Size: 4
    Vector m_vMinimapMins; // Size: 12
    Vector m_vMinimapMaxs; // Size: 12
    char m_MinimapVerticalSectionHeights[32];
    bool m_bSpawnedTerrorHuntHeavy; // Size: 4
    char m_pad3_3164[3];
    char m_nEndMatchMapGroupVoteTypes[40];
    char m_nEndMatchMapGroupVoteOptions[40];
    int32 m_nEndMatchMapVoteWinner; // Size: 4
    int32 m_iNumConsecutiveCTLoses; // Size: 4
    int32 m_iNumConsecutiveTerroristLoses; // Size: 28
    char m_pad24_3280[24];
    bool m_bMarkClientStopRecordAtRoundEnd; // Size: 168
    char m_pad167_3448[167];
    int32 m_nMatchAbortedEarlyReason; // Size: 4
    bool m_bHasTriggeredRoundStartMusic; // Size: 1
    bool m_bSwitchingTeamsAtRoundReset; // Size: 27
    char m_pad26_3480[26];
    CCSGameModeRules* m_pGameModeRules; // Size: 8
    C_RetakeGameRules m_RetakeRules; // Size: 280
    uint8 m_nMatchEndCount; // Size: 4
    char m_pad3_3772[3];
    int32 m_nTTeamIntroVariant; // Size: 4
    int32 m_nCTTeamIntroVariant; // Size: 4
    bool m_bTeamIntroPeriod; // Size: 4
    char m_pad3_3784[3];
    int32 m_iRoundEndWinnerTeam; // Size: 4
    int32 m_eRoundEndReason; // Size: 4
    bool m_bRoundEndShowTimerDefend; // Size: 4
    char m_pad3_3796[3];
    int32 m_iRoundEndTimerTime; // Size: 4
    void* m_sRoundEndFunFactToken;
    char m_iRoundEndFunFactPlayerSlot[4];
    int32 m_iRoundEndFunFactData1; // Size: 4
    int32 m_iRoundEndFunFactData2; // Size: 4
    int32 m_iRoundEndFunFactData3; // Size: 4
    void* m_sRoundEndMessage;
    int32 m_iRoundEndPlayerCount; // Size: 4
    bool m_bRoundEndNoMusic; // Size: 4
    char m_pad3_3840[3];
    int32 m_iRoundEndLegacy; // Size: 4
    uint8 m_nRoundEndCount; // Size: 4
    char m_pad3_3848[3];
    int32 m_iRoundStartRoundNumber; // Size: 4
    uint8 m_nRoundStartCount; // Size: 16396
    char m_pad16395_20248[16395];
};

struct __declspec(align(8)) C_CSGameRulesProxy {
    char m_pad[1384];
};

struct __declspec(align(8)) CCSGameModeRules {
    char m_pad[8];
};

struct  C_RetakeGameRules {
    char m_pad[248];
    int32 m_nMatchSeed; // Size: 4
    bool m_bBlockersPresent; // Size: 1
    bool m_bRoundInProgress; // Size: 3
    char m_pad2_256[2];
    int32 m_iFirstSecondHalfRound; // Size: 4
};

struct __declspec(align(8)) CCSGameModeRules_Noop {
};

struct __declspec(align(8)) CCSGameModeRules_ArmsRace {
    char m_pad[48];
};

struct __declspec(align(8)) CCSGameModeRules_Deathmatch {
    char m_pad[48];
    char m_flDMBonusStartTime[4];
    float32 m_flDMBonusTimeLength; // Size: 4
};

struct  CSPerRoundStats_t {
    char m_pad[48];
    int32 m_iKills; // Size: 4
    int32 m_iDeaths; // Size: 4
    int32 m_iAssists; // Size: 4
    int32 m_iDamage; // Size: 4
    int32 m_iEquipmentValue; // Size: 4
    int32 m_iMoneySaved; // Size: 4
    int32 m_iKillReward; // Size: 4
    int32 m_iLiveTime; // Size: 4
    int32 m_iHeadShotKills; // Size: 4
    int32 m_iObjective; // Size: 4
    int32 m_iCashEarned; // Size: 4
    int32 m_iUtilityDamage; // Size: 4
};

struct  CSMatchStats_t {
    char m_pad[104];
    int32 m_iEnemy5Ks; // Size: 4
    int32 m_iEnemy4Ks; // Size: 4
    int32 m_iEnemy3Ks; // Size: 4
    int32 m_iEnemyKnifeKills; // Size: 4
};

struct  C_CSGO_TeamPreviewCharacterPosition {
    char m_pad[1384];
    int32 m_nVariant; // Size: 4
    int32 m_nRandom; // Size: 4
    int32 m_nOrdinal; // Size: 8
    char m_pad4_1400[4];
    void* m_sWeaponName;
    uint64 m_xuid; // Size: 8
    C_EconItemView m_agentItem; // Size: 1096
    C_EconItemView m_glovesItem; // Size: 1096
};

struct  C_CSGO_TeamSelectCharacterPosition {
};

struct __declspec(align(8)) C_CSGO_TeamSelectTerroristPosition {
};

struct __declspec(align(8)) C_CSGO_TeamSelectCounterTerroristPosition {
};

struct  C_CSGO_TeamIntroCharacterPosition {
};

struct __declspec(align(8)) C_CSGO_TeamIntroTerroristPosition {
};

struct __declspec(align(8)) C_CSGO_TeamIntroCounterTerroristPosition {
};

struct  CCSGO_WingmanIntroCharacterPosition {
};

struct __declspec(align(8)) CCSGO_WingmanIntroTerroristPosition {
};

struct __declspec(align(8)) CCSGO_WingmanIntroCounterTerroristPosition {
};

struct __declspec(align(8)) C_CSMinimapBoundary {
};

struct __declspec(align(8)) CCSPointScriptEntity {
};

struct __declspec(align(8)) CCSClientPointScriptEntity {
};

struct  CCSPointScript {
    char m_pad[248];
};

struct  CCSPointScriptExtensions_entity {
};

struct  CCSPointScriptExtensions_player {
};

struct  CCSPointScriptExtensions_observer {
};

struct  CCSPointScriptExtensions_player_controller {
};

struct  CCSPointScriptExtensions_weapon_cs_base {
};

struct  CCSPointScriptExtensions_CCSWeaponBaseVData {
};

struct  PredictedDamageTag_t {
    char m_pad[48];
    char nTagTick[4];
    float32 flFlinchModSmall; // Size: 4
    float32 flFlinchModLarge; // Size: 4
};

struct __declspec(align(16)) C_CSPlayerPawn {
    char m_pad[5400];
    CCSPlayer_BulletServices* m_pBulletServices; // Size: 8
    CCSPlayer_HostageServices* m_pHostageServices; // Size: 8
    CCSPlayer_BuyServices* m_pBuyServices; // Size: 8
    CCSPlayer_GlowServices* m_pGlowServices; // Size: 8
    CCSPlayer_ActionTrackingServices* m_pActionTrackingServices; // Size: 8
    CCSPlayer_DamageReactServices* m_pDamageReactServices; // Size: 8
    char m_flHealthShotBoostExpirationTime[4];
    char m_flLastFiredWeaponTime[4];
    bool m_bHasFemaleVoice; // Size: 4
    char m_pad3_5460[3];
    float32 m_flLandingTimeSeconds; // Size: 4
    float32 m_flOldFallVelocity; // Size: 4
    char m_szLastPlaceName[18];
    bool m_bPrevDefuser; // Size: 1
    bool m_bPrevHelmet; // Size: 1
    int32 m_nPrevArmorVal; // Size: 4
    int32 m_nPrevGrenadeAmmoCount; // Size: 4
    uint32 m_unPreviousWeaponHash; // Size: 4
    uint32 m_unWeaponHash; // Size: 4
    bool m_bInBuyZone; // Size: 1
    bool m_bPreviouslyInBuyZone; // Size: 3
    char m_pad2_5508[2];
    QAngle m_aimPunchAngle; // Size: 12
    QAngle m_aimPunchAngleVel; // Size: 12
    int32 m_aimPunchTickBase; // Size: 4
    float32 m_aimPunchTickFraction; // Size: 8
    char m_pad4_5544[4];
    char m_aimPunchCache[32];
    bool m_bInLanding; // Size: 4
    char m_pad3_5580[3];
    float32 m_flLandingStartTime; // Size: 4
    bool m_bInHostageRescueZone; // Size: 1
    bool m_bInBombZone; // Size: 1
    bool m_bIsBuyMenuOpen; // Size: 2
    char m_pad1_5588[1];
    char m_flTimeOfLastInjury[4];
    char m_flNextSprayDecalTime[312];
    int32 m_iRetakesOffering; // Size: 4
    int32 m_iRetakesOfferingCard; // Size: 4
    bool m_bRetakesHasDefuseKit; // Size: 1
    bool m_bRetakesMVPLastRound; // Size: 3
    char m_pad2_5916[2];
    int32 m_iRetakesMVPBoostItem; // Size: 4
    char m_RetakesMVPBoostExtraUtility[32];
    bool m_bNeedToReApplyGloves; // Size: 8
    char m_pad7_5960[7];
    C_EconItemView m_EconGloves; // Size: 1096
    uint8 m_nEconGlovesChanged; // Size: 1
    bool m_bMustSyncRagdollState; // Size: 3
    char m_pad2_7060[2];
    int32 m_nRagdollDamageBone; // Size: 4
    Vector m_vRagdollDamageForce; // Size: 12
    Vector m_vRagdollDamagePosition; // Size: 12
    char m_szRagdollDamageWeaponName[64];
    bool m_bRagdollDamageHeadshot; // Size: 4
    char m_pad3_7156[3];
    Vector m_vRagdollServerOrigin; // Size: 1668
    bool m_bLastHeadBoneTransformIsValid; // Size: 4
    char m_pad3_8828[3];
    char m_lastLandTime[4];
    bool m_bOnGroundLastTick; // Size: 28
    char m_pad27_8860[27];
    QAngle m_qDeathEyeAngles; // Size: 12
    bool m_bSkipOneHeadConstraintUpdate; // Size: 1
    bool m_bLeftHanded; // Size: 3
    char m_pad2_8876[2];
    char m_fSwitchedHandednessTime[4];
    float32 m_flViewmodelOffsetX; // Size: 4
    float32 m_flViewmodelOffsetY; // Size: 4
    float32 m_flViewmodelOffsetZ; // Size: 4
    float32 m_flViewmodelFOV; // Size: 4
    char m_vecPlayerPatchEconIndices[56];
    Color m_GunGameImmunityColor; // Size: 80
    char m_vecBulletHitModels[24];
    bool m_bIsWalking; // Size: 8
    char m_pad7_9064[7];
    QAngle m_thirdPersonHeading; // Size: 24
    float32 m_flSlopeDropOffset; // Size: 16
    char m_pad12_9104[12];
    float32 m_flSlopeDropHeight; // Size: 16
    char m_pad12_9120[12];
    Vector m_vHeadConstraintOffset; // Size: 24
    EntitySpottedState_t m_entitySpottedState; // Size: 24
    bool m_bIsScoped; // Size: 1
    bool m_bResumeZoom; // Size: 1
    bool m_bIsDefusing; // Size: 1
    bool m_bIsGrabbingHostage; // Size: 1
    char m_iBlockingUseActionInProgress[4];
    char m_flEmitSoundTime[4];
    bool m_bInNoDefuseArea; // Size: 4
    char m_pad3_9184[3];
    int32 m_nWhichBombZone; // Size: 4
    int32 m_iShotsFired; // Size: 4
    float32 m_flFlinchStack; // Size: 4
    float32 m_flVelocityModifier; // Size: 4
    float32 m_flHitHeading; // Size: 4
    int32 m_nHitBodyPart; // Size: 4
    bool m_bWaitForNoAttack; // Size: 4
    char m_pad3_9212[3];
    float32 m_ignoreLadderJumpTime; // Size: 5
    char m_pad1_9217[1];
    bool m_bKilledByHeadshot; // Size: 3
    char m_pad2_9220[2];
    int32 m_ArmorValue; // Size: 4
    uint16 m_unCurrentEquipmentValue; // Size: 2
    uint16 m_unRoundStartEquipmentValue; // Size: 2
    uint16 m_unFreezetimeEndEquipmentValue; // Size: 4
    char m_pad2_9232[2];
    char m_nLastKillerIndex[4];
    bool m_bOldIsScoped; // Size: 1
    bool m_bHasDeathInfo; // Size: 3
    char m_pad2_9240[2];
    float32 m_flDeathInfoTime; // Size: 4
    Vector m_vecDeathInfoOrigin; // Size: 12
    char m_grenadeParameterStashTime[4];
    bool m_bGrenadeParametersStashed; // Size: 4
    char m_pad3_9264[3];
    QAngle m_angStashedShootAngles; // Size: 12
    Vector m_vecStashedGrenadeThrowPosition; // Size: 12
    Vector m_vecStashedVelocity; // Size: 12
    char m_angShootAngleHistory[24];
    char m_vecThrowPositionHistory[24];
    char m_vecVelocityHistory[28];
    char m_PredictedDamageTags[80];
    char m_nPrevHighestReceivedDamageTagTick[4];
};

struct __declspec(align(8)) C_PlayerPing {
    char m_pad[1432];
    char m_hPlayer[4];
    char m_hPingedEntity[4];
    int32 m_iType; // Size: 4
    bool m_bUrgent; // Size: 1
};

struct  CCSPlayer_PingServices {
    char m_pad[64];
};

struct __declspec(align(8)) C_CSPlayerResource {
    char m_pad[1384];
    char m_bHostageAlive[12];
    char m_isHostageFollowingSomeone[12];
    char m_iHostageEntityIDs[48];
    Vector m_bombsiteCenterA; // Size: 12
    Vector m_bombsiteCenterB; // Size: 12
    char m_hostageRescueX[16];
    char m_hostageRescueY[16];
    char m_hostageRescueZ[16];
    bool m_bEndMatchNextMapAllVoted; // Size: 1
};

struct  CCSPlayer_DamageReactServices {
};

struct  CPlayer_ViewModelServices {
};

struct  CCSPlayerBase_CameraServices {
    char m_pad[528];
    uint32 m_iFOV; // Size: 4
    uint32 m_iFOVStart; // Size: 4
    char m_flFOVTime[4];
    float32 m_flFOVRate; // Size: 4
    char m_hZoomOwner[4];
};

struct  WeaponPurchaseCount_t {
    char m_pad[48];
    uint16 m_nItemDefIndex; // Size: 2
};

struct  WeaponPurchaseTracker_t {
    char m_pad[8];
};

struct  CCSPlayer_ActionTrackingServices {
    char m_pad[64];
    char m_hLastWeaponBeforeC4AutoSwitch[4];
    bool m_bIsRescuing; // Size: 4
    char m_pad3_72[3];
    WeaponPurchaseTracker_t m_weaponPurchasesThisMatch; // Size: 88
};

struct  CCSPlayer_BulletServices {
    char m_pad[64];
};

struct  SellbackPurchaseEntry_t {
    char m_pad[48];
    uint16 m_unDefIdx; // Size: 4
    char m_pad2_52[2];
    int32 m_nCost; // Size: 4
    int32 m_nPrevArmor; // Size: 4
    bool m_bPrevHelmet; // Size: 4
    char m_pad3_64[3];
};

struct  CCSPlayer_BuyServices {
    char m_pad[64];
};

struct  CCSPlayer_CameraServices {
    char m_pad[552];
    float32 m_flDeathCamTilt; // Size: 8
    char m_pad4_560[4];
};

struct  CCSPlayer_HostageServices {
    char m_pad[64];
    char m_hCarriedHostage[4];
};

struct  CCSPlayer_ItemServices {
    char m_pad[64];
    bool m_bHasDefuser; // Size: 1
    bool m_bHasHelmet; // Size: 1
};

struct  CCSPlayer_MovementServices {
    char m_pad[536];
    float32 m_flMaxFallVelocity; // Size: 4
    Vector m_vecLadderNormal; // Size: 12
    int32 m_nLadderSurfacePropIndex; // Size: 4
    float32 m_flDuckAmount; // Size: 4
    float32 m_flDuckSpeed; // Size: 4
    bool m_bDuckOverride; // Size: 1
    bool m_bDesiresDuck; // Size: 3
    char m_pad2_568[2];
    float32 m_flDuckOffset; // Size: 4
    uint32 m_nDuckTimeMsecs; // Size: 4
    uint32 m_nDuckJumpTimeMsecs; // Size: 4
    uint32 m_nJumpTimeMsecs; // Size: 4
    float32 m_flLastDuckTime; // Size: 16
    char m_pad12_600[12];
    void* m_vecLastPositionAtFullCrouchSpeed;
    bool m_duckUntilOnGround; // Size: 1
    bool m_bHasWalkMovedSinceLastJump; // Size: 1
    bool m_bInStuckTest; // Size: 14
    char m_pad13_624[13];
    char m_flStuckCheckTime[512];
    int32 m_nTraceCount; // Size: 4
    int32 m_StuckLast; // Size: 4
    bool m_bSpeedCropped; // Size: 4
    char m_pad3_1148[3];
    float32 m_flGroundMoveEfficiency; // Size: 4
    int32 m_nOldWaterLevel; // Size: 4
    float32 m_flWaterEntryTime; // Size: 4
    Vector m_vecForward; // Size: 12
    Vector m_vecLeft; // Size: 12
    Vector m_vecUp; // Size: 12
    int32 m_nGameCodeHasMovedPlayerAfterCommand; // Size: 4
    bool m_bOldJumpPressed; // Size: 4
    char m_pad3_1204[3];
    float32 m_flJumpPressedTime; // Size: 4
    float32 m_flJumpUntil; // Size: 4
    float32 m_flJumpVel; // Size: 4
    void* m_fStashGrenadeParameterWhen;
    uint64 m_nButtonDownMaskPrev; // Size: 8
    float32 m_flOffsetTickCompleteTime; // Size: 4
    float32 m_flOffsetTickStashedSpeed; // Size: 4
    float32 m_flStamina; // Size: 4
    float32 m_flHeightAtJumpStart; // Size: 4
    float32 m_flMaxJumpHeightThisJump; // Size: 4
};

struct  CCSPlayer_UseServices {
};

struct __declspec(align(8)) C_BaseViewModel {
    char m_pad[3984];
    Vector m_vecLastFacing; // Size: 12
    uint32 m_nViewModelIndex; // Size: 4
    uint32 m_nAnimationParity; // Size: 4
    float32 m_flAnimationStartTime; // Size: 4
    void* m_hWeapon;
    void* m_sVMName;
    void* m_sAnimationPrefix;
    char m_iCameraAttachment[4];
    QAngle m_vecLastCameraAngles; // Size: 12
    float32 m_previousElapsedDuration; // Size: 4
    float32 m_previousCycle; // Size: 4
    int32 m_nOldAnimationParity; // Size: 4
    char m_hOldLayerSequence[4];
    int32 m_oldLayer; // Size: 4
    float32 m_oldLayerStartTime; // Size: 4
};

struct  CCSPlayer_ViewModelServices {
    char m_pad[64];
};

struct  CCSPlayer_WaterServices {
    char m_pad[64];
    float32 m_flWaterJumpTime; // Size: 4
    Vector m_vecWaterJumpVel; // Size: 12
};

struct  CCSPlayer_WeaponServices {
    char m_pad[184];
    char m_flNextAttack[4];
    bool m_bIsLookingAtWeapon; // Size: 1
    bool m_bIsHoldingLookAtWeapon; // Size: 3
    char m_pad2_192[2];
    uint32 m_nOldShootPositionHistoryCount; // Size: 920
    char m_pad916_1112[916];
};

struct  CCSObserver_ObserverServices {
    char m_pad[88];
    char m_hLastObserverTarget[4];
    Vector m_vecObserverInterpolateOffset; // Size: 12
    Vector m_vecObserverInterpStartPos; // Size: 12
    float32 m_flObsInterp_PathLength; // Size: 12
    char m_pad8_128[8];
    char m_qObsInterp_OrientationStart[16];
    char m_qObsInterp_OrientationTravelDir[16];
    char m_obsInterpState[4];
};

struct  CCSObserver_CameraServices {
};

struct  CCSObserver_MovementServices {
};

struct  CCSObserver_UseServices {
};

struct  CCSObserver_ViewModelServices {
};

struct  CCSPlayerController_ActionTrackingServices {
    char m_pad[64];
    char m_perRoundStats[80];
    CSMatchStats_t m_matchStats; // Size: 128
    int32 m_iNumRoundKills; // Size: 4
    int32 m_iNumRoundKillsHeadshots; // Size: 4
};

struct __declspec(align(8)) CCSPlayerController {
    char m_pad[1824];
    CCSPlayerController_InGameMoneyServices* m_pInGameMoneyServices; // Size: 8
    CCSPlayerController_InventoryServices* m_pInventoryServices; // Size: 8
    CCSPlayerController_ActionTrackingServices* m_pActionTrackingServices; // Size: 8
    CCSPlayerController_DamageServices* m_pDamageServices; // Size: 8
    uint32 m_iPing; // Size: 4
    bool m_bHasCommunicationAbuseMute; // Size: 4
    char m_pad3_1864[3];
    void* m_szCrosshairCodes;
    uint8 m_iPendingTeamNum; // Size: 4
    char m_pad3_1876[3];
    char m_flForceTeamTime[4];
    int32 m_iCompTeammateColor; // Size: 4
    bool m_bEverPlayedOnTeam; // Size: 4
    char m_pad3_1888[3];
    void* m_flPreviousForceJoinTeamTime;
    void* m_szClan;
    void* m_sSanitizedPlayerName;
    int32 m_iCoachingTeam; // Size: 8
    char m_pad4_1920[4];
    uint64 m_nPlayerDominated; // Size: 8
    uint64 m_nPlayerDominatingMe; // Size: 8
    int32 m_iCompetitiveRanking; // Size: 4
    int32 m_iCompetitiveWins; // Size: 4
    int8 m_iCompetitiveRankType; // Size: 4
    char m_pad3_1948[3];
    int32 m_iCompetitiveRankingPredicted_Win; // Size: 4
    int32 m_iCompetitiveRankingPredicted_Loss; // Size: 4
    int32 m_iCompetitiveRankingPredicted_Tie; // Size: 4
    int32 m_nEndMatchNextMapVote; // Size: 4
    uint16 m_unActiveQuestId; // Size: 4
    char m_pad2_1968[2];
    char m_nQuestProgressReason[4];
    uint32 m_unPlayerTvControlFlags; // Size: 44
    char m_pad40_2016[40];
    int32 m_iDraftIndex; // Size: 4
    uint32 m_msQueuedModeDisconnectionTimestamp; // Size: 4
    uint32 m_uiAbandonRecordedReason; // Size: 4
    bool m_bCannotBeKicked; // Size: 1
    bool m_bEverFullyConnected; // Size: 1
    bool m_bAbandonAllowsSurrender; // Size: 1
    bool m_bAbandonOffersInstantSurrender; // Size: 1
    bool m_bDisconnection1MinWarningPrinted; // Size: 1
    bool m_bScoreReported; // Size: 3
    char m_pad2_2036[2];
    int32 m_nDisconnectionTick; // Size: 12
    char m_pad8_2048[8];
    bool m_bControllingBot; // Size: 1
    bool m_bHasControlledBotThisRound; // Size: 1
    bool m_bHasBeenControlledByPlayerThisRound; // Size: 2
    char m_pad1_2052[1];
    int32 m_nBotsControlledThisRound; // Size: 4
    bool m_bCanControlObservedBot; // Size: 4
    char m_pad3_2060[3];
    char m_hPlayerPawn[4];
    char m_hObserverPawn[4];
    bool m_bPawnIsAlive; // Size: 4
    char m_pad3_2072[3];
    uint32 m_iPawnHealth; // Size: 4
    int32 m_iPawnArmor; // Size: 4
    bool m_bPawnHasDefuser; // Size: 1
    bool m_bPawnHasHelmet; // Size: 1
    uint16 m_nPawnCharacterDefIndex; // Size: 2
    int32 m_iPawnLifetimeStart; // Size: 4
    int32 m_iPawnLifetimeEnd; // Size: 4
    int32 m_iPawnBotDifficulty; // Size: 4
    char m_hOriginalControllerOfCurrentPawn[4];
    int32 m_iScore; // Size: 4
    char m_vecKills[24];
    bool m_bMvpNoMusic; // Size: 4
    char m_pad3_2132[3];
    int32 m_eMvpReason; // Size: 4
    int32 m_iMusicKitID; // Size: 4
    int32 m_iMusicKitMVPs; // Size: 4
    int32 m_iMVPs; // Size: 4
};

struct  CDamageRecord {
    char m_pad[40];
    char m_PlayerDamager[4];
    char m_PlayerRecipient[4];
    char m_hPlayerControllerDamager[4];
    char m_hPlayerControllerRecipient[4];
    void* m_szPlayerDamagerName;
    void* m_szPlayerRecipientName;
    uint64 m_DamagerXuid; // Size: 8
    uint64 m_RecipientXuid; // Size: 8
    int32 m_iBulletsDamage; // Size: 4
    int32 m_iDamage; // Size: 4
    int32 m_iActualHealthRemoved; // Size: 4
    int32 m_iNumHits; // Size: 4
    int32 m_iLastBulletUpdate; // Size: 4
    bool m_bIsOtherEnemy; // Size: 1
};

struct  CCSPlayerController_DamageServices {
    char m_pad[64];
    int32 m_nSendUpdate; // Size: 8
    char m_pad4_72[4];
};

struct  CCSPlayerController_InGameMoneyServices {
    char m_pad[64];
    int32 m_iAccount; // Size: 4
    int32 m_iStartAccount; // Size: 4
    int32 m_iTotalCashSpent; // Size: 4
};

struct  ServerAuthoritativeWeaponSlot_t {
    char m_pad[40];
    uint16 unClass; // Size: 2
    uint16 unSlot; // Size: 2
};

struct  CCSPlayerController_InventoryServices {
    char m_pad[64];
    uint16 m_unMusicID; // Size: 4
    char m_pad2_68[2];
    char m_rank[24];
    int32 m_nPersonaDataPublicLevel; // Size: 4
    int32 m_nPersonaDataPublicCommendsLeader; // Size: 4
    int32 m_nPersonaDataPublicCommendsTeacher; // Size: 4
    int32 m_nPersonaDataPublicCommendsFriendly; // Size: 4
    int32 m_nPersonaDataXpTrailLevel; // Size: 4
};

struct  C_IronSightController {
    char m_pad[16];
    bool m_bIronSightAvailable; // Size: 4
    char m_pad3_20[3];
    float32 m_flIronSightAmount; // Size: 4
    float32 m_flIronSightAmountGained; // Size: 4
    float32 m_flIronSightAmountBiased; // Size: 4
    float32 m_flIronSightAmount_Interpolated; // Size: 4
    float32 m_flIronSightAmountGained_Interpolated; // Size: 4
    float32 m_flIronSightAmountBiased_Interpolated; // Size: 4
    float32 m_flInterpolationLastUpdated; // Size: 4
    char m_angDeltaAverage[96];
    QAngle m_angViewLast; // Size: 12
    void* m_vecDotCoords;
    float32 m_flDotBlur; // Size: 4
};

struct __declspec(align(8)) CompositeMaterialMatchFilter_t {
    void* m_nCompositeMaterialMatchFilterType;
    char m_pad[8];
    void* m_strMatchFilter;
    void* m_strMatchValue;
};

struct __declspec(align(8)) CompositeMaterialInputLooseVariable_t {
    void* m_strName;
    char m_pad[8];
    bool m_bExposeExternally; // Size: 8
    char m_pad7_16[7];
    void* m_strExposedFriendlyName;
    void* m_strExposedFriendlyGroupName;
    bool m_bExposedVariableIsFixedRange; // Size: 8
    char m_pad7_40[7];
    void* m_strExposedVisibleWhenTrue;
    void* m_strExposedHiddenWhenTrue;
    char m_nVariableType[4];
    bool m_bValueBoolean; // Size: 4
    char m_pad3_64[3];
    int32 m_nValueIntX; // Size: 4
    int32 m_nValueIntY; // Size: 4
    int32 m_nValueIntZ; // Size: 4
    int32 m_nValueIntW; // Size: 4
    bool m_bHasFloatBounds; // Size: 4
    char m_pad3_84[3];
    float32 m_flValueFloatX; // Size: 4
    float32 m_flValueFloatX_Min; // Size: 4
    float32 m_flValueFloatX_Max; // Size: 4
    float32 m_flValueFloatY; // Size: 4
    float32 m_flValueFloatY_Min; // Size: 4
    float32 m_flValueFloatY_Max; // Size: 4
    float32 m_flValueFloatZ; // Size: 4
    float32 m_flValueFloatZ_Min; // Size: 4
    float32 m_flValueFloatZ_Max; // Size: 4
    float32 m_flValueFloatW; // Size: 4
    float32 m_flValueFloatW_Min; // Size: 4
    float32 m_flValueFloatW_Max; // Size: 4
    Color m_cValueColor4; // Size: 4
    void* m_nValueSystemVar;
    char m_strResourceMaterial[224];
    void* m_strTextureContentAssetPath;
    char m_strTextureRuntimeResourcePath[224];
    void* m_strTextureCompilationVtexTemplate;
    void* m_nTextureType;
    void* m_strString;
    void* m_strPanoramaPanelPath;
};

struct __declspec(align(8)) CompMatMutatorCondition_t {
    void* m_nMutatorCondition;
    char m_pad[8];
    void* m_strMutatorConditionContainerName;
    void* m_strMutatorConditionContainerVarName;
    void* m_strMutatorConditionContainerVarValue;
};

struct __declspec(align(8)) CompMatPropertyMutator_t {
    bool m_bEnabled; // Size: 4
    char m_pad3_4[3];
    char m_pad[4];
    char m_nMutatorCommandType[4];
    void* m_strInitWith_Container;
    void* m_strCopyProperty_InputContainerSrc;
    void* m_strCopyProperty_InputContainerProperty;
    void* m_strCopyProperty_TargetProperty;
    void* m_strRandomRollInputVars_SeedInputVar;
    char m_vecRandomRollInputVars_InputVarsToRoll[24];
    void* m_strCopyMatchingKeys_InputContainerSrc;
    void* m_strCopyKeysWithSuffix_InputContainerSrc;
    void* m_strCopyKeysWithSuffix_FindSuffix;
    void* m_strCopyKeysWithSuffix_ReplaceSuffix;
    CompositeMaterialInputLooseVariable_t m_nSetValue_Value; // Size: 640
    void* m_strGenerateTexture_TargetParam;
    void* m_strGenerateTexture_InitialContainer;
    int32 m_nResolution; // Size: 4
    bool m_bIsScratchTarget; // Size: 1
    bool m_bSplatDebugInfo; // Size: 1
    bool m_bCaptureInRenderDoc; // Size: 2
    char m_pad1_768[1];
    char m_vecTexGenInstructions[24];
    char m_vecConditionalMutators[24];
    void* m_strPopInputQueue_Container;
    void* m_strDrawText_InputContainerSrc;
    void* m_strDrawText_InputContainerProperty;
    void* m_vecDrawText_Position;
    Color m_colDrawText_Color; // Size: 8
    void* m_strDrawText_Font;
};

struct __declspec(align(8)) CompositeMaterialInputContainer_t {
    bool m_bEnabled; // Size: 4
    char m_pad3_4[3];
    char m_pad[4];
    char m_nCompositeMaterialInputContainerSourceType[4];
    char m_strSpecificContainerMaterial[224];
    void* m_strAttrName;
    void* m_strAlias;
    char m_vecLooseVariables[24];
    void* m_strAttrNameForVar;
};

struct __declspec(align(8)) CompositeMaterialAssemblyProcedure_t {
    char m_vecCompMatIncludes[24];
    char m_pad[24];
    char m_vecMatchFilters[24];
    char m_vecCompositeInputContainers[24];
};

struct  GeneratedTextureHandle_t {
};

struct  CompositeMaterial_t {
    char m_pad[8];
    char m_TargetKVs[16];
    char m_PreGenerationKVs[64];
    char m_FinalKVs[40];
};

struct __declspec(align(8)) CompositeMaterialEditorPoint_t {
    char m_ModelName[224];
    char m_pad[224];
    int32 m_nSequenceIndex; // Size: 4
    float32 m_flCycle; // Size: 4
    char m_KVModelStateChoices[16];
    bool m_bEnableChildModel; // Size: 8
    char m_pad7_256[7];
    char m_ChildModelName[224];
    char m_vecCompositeMaterialAssemblyProcedures[24];
};

struct __declspec(align(8)) CCompositeMaterialEditorDoc {
    char m_pad[8];
    int32 m_nVersion; // Size: 8
    char m_pad4_16[4];
    char m_Points[24];
};

struct  CGlobalLightBase {
    char m_pad[16];
    bool m_bSpotLight; // Size: 4
    char m_pad3_20[3];
    Vector m_SpotLightOrigin; // Size: 12
    QAngle m_SpotLightAngles; // Size: 12
    Vector m_ShadowDirection; // Size: 12
    Vector m_AmbientDirection; // Size: 12
    Vector m_SpecularDirection; // Size: 12
    Vector m_InspectorSpecularDirection; // Size: 12
    float32 m_flSpecularPower; // Size: 4
    float32 m_flSpecularIndependence; // Size: 4
    Color m_SpecularColor; // Size: 4
    bool m_bStartDisabled; // Size: 1
    bool m_bEnabled; // Size: 1
    Color m_LightColor; // Size: 4
    Color m_AmbientColor1; // Size: 4
    Color m_AmbientColor2; // Size: 4
    Color m_AmbientColor3; // Size: 6
    float32 m_flSunDistance; // Size: 4
    float32 m_flFOV; // Size: 4
    float32 m_flNearZ; // Size: 4
    float32 m_flFarZ; // Size: 4
    bool m_bEnableShadows; // Size: 1
    bool m_bOldEnableShadows; // Size: 1
    bool m_bBackgroundClearNotRequired; // Size: 2
    char m_pad1_144[1];
    float32 m_flCloudScale; // Size: 4
    float32 m_flCloud1Speed; // Size: 4
    float32 m_flCloud1Direction; // Size: 4
    float32 m_flCloud2Speed; // Size: 4
    float32 m_flCloud2Direction; // Size: 16
    char m_pad12_176[12];
    float32 m_flAmbientScale1; // Size: 4
    float32 m_flAmbientScale2; // Size: 4
    float32 m_flGroundScale; // Size: 4
    float32 m_flLightScale; // Size: 4
    float32 m_flFoWDarkness; // Size: 4
    bool m_bEnableSeparateSkyboxFog; // Size: 4
    char m_pad3_200[3];
    Vector m_vFowColor; // Size: 12
    Vector m_ViewOrigin; // Size: 12
    QAngle m_ViewAngles; // Size: 12
    float32 m_flViewFoV; // Size: 4
    char m_WorldPoints[952];
    void* m_vFogOffsetLayer0;
    void* m_vFogOffsetLayer1;
    char m_hEnvWind[4];
};

struct __declspec(align(16)) C_GlobalLight {
    char m_pad[2608];
};

struct  C_CSGO_PreviewModel_GraphController {
    char m_pad[96];
    char m_pszCharacterMode[40];
    char m_pszWeaponState[40];
    char m_pszWeaponType[40];
};

struct  C_CSGO_PreviewPlayer_GraphController {
    char m_pad[96];
    char m_pszCharacterMode[40];
    char m_pszTeamPreviewVariant[40];
    char m_pszTeamPreviewPosition[40];
    char m_pszEndOfMatchCelebration[40];
    char m_nTeamPreviewRandom[32];
    char m_pszWeaponState[40];
    char m_pszWeaponType[40];
};

struct __declspec(align(8)) C_CSGO_MapPreviewCameraPathNode {
    char m_pad[1384];
    void* m_szParentPathUniqueID;
    int32 m_nPathIndex; // Size: 4
    Vector m_vInTangentLocal; // Size: 12
    Vector m_vOutTangentLocal; // Size: 12
    float32 m_flFOV; // Size: 4
    float32 m_flCameraSpeed; // Size: 4
    float32 m_flEaseIn; // Size: 4
    float32 m_flEaseOut; // Size: 4
    Vector m_vInTangentWorld; // Size: 12
};

struct __declspec(align(8)) C_CSGO_MapPreviewCameraPath {
    char m_pad[1384];
    float32 m_flZFar; // Size: 4
    float32 m_flZNear; // Size: 4
    bool m_bLoop; // Size: 1
    bool m_bVerticalFOV; // Size: 1
    bool m_bConstantSpeed; // Size: 2
    char m_pad1_1396[1];
    float32 m_flDuration; // Size: 68
    char m_pad64_1464[64];
    float32 m_flPathLength; // Size: 4
};

struct  CCSPlayer_GlowServices {
};

struct __declspec(align(8)) C_VoteController {
    char m_pad[1400];
    int32 m_iActiveIssueIndex; // Size: 4
    int32 m_iOnlyTeamToVote; // Size: 4
    char m_nVoteOptionCount[20];
    int32 m_nPotentialVotes; // Size: 4
    bool m_bVotesDirty; // Size: 1
    bool m_bTypeDirty; // Size: 1
};

struct __declspec(align(8)) C_MapVetoPickController {
    char m_pad[1400];
    int32 m_nDraftType; // Size: 4
    int32 m_nTeamWinningCoinToss; // Size: 4
    char m_nTeamWithFirstChoice[256];
    char m_nVoteMapIdsList[28];
    char m_nAccountIDs[256];
    char m_nMapId0[256];
    char m_nMapId1[256];
    char m_nMapId2[256];
    char m_nMapId3[256];
    char m_nMapId4[256];
    char m_nMapId5[256];
    char m_nStartingSide0[256];
    int32 m_nCurrentPhase; // Size: 4
    int32 m_nPhaseStartTick; // Size: 4
    int32 m_nPhaseDurationTicks; // Size: 4
    int32 m_nPostDataUpdateTick; // Size: 4
};

struct  CPlayerSprayDecalRenderHelper {
};

struct  C_CSGO_TeamPreviewCamera {
    char m_pad[1488];
    int32 m_nVariant; // Size: 4
    bool m_bDofEnabled; // Size: 4
    char m_pad3_1496[3];
    float32 m_flDofNearBlurry; // Size: 4
    float32 m_flDofNearCrisp; // Size: 4
    float32 m_flDofFarCrisp; // Size: 4
    float32 m_flDofFarBlurry; // Size: 4
};

struct __declspec(align(8)) C_CSGO_TeamSelectCamera {
};

struct __declspec(align(8)) C_CSGO_TerroristTeamIntroCamera {
};

struct __declspec(align(8)) C_CSGO_TerroristWingmanIntroCamera {
};

struct __declspec(align(8)) C_CSGO_CounterTerroristTeamIntroCamera {
};

struct __declspec(align(8)) C_CSGO_CounterTerroristWingmanIntroCamera {
};

struct __declspec(align(8)) C_CSGO_EndOfMatchCamera {
};

struct __declspec(align(8)) C_CSGO_EndOfMatchCharacterPosition {
};

struct  C_CSGO_EndOfMatchLineupEndpoint {
};

struct __declspec(align(8)) C_CSGO_EndOfMatchLineupStart {
};

struct __declspec(align(8)) C_CSGO_EndOfMatchLineupEnd {
};

struct __declspec(align(8)) C_CsmFovOverride {
    char m_pad[1384];
    void* m_cameraName;
};

struct  C_Chicken_GraphController {
    char m_pad[96];
    char m_paramActivity[40];
    char m_paramEndActivityImmediately[32];
    char m_paramSnapToSquatting[32];
    char m_sActivityFinished[24];
};

struct __declspec(align(8)) C_PointEntity {
};

struct __declspec(align(8)) C_EnvCombinedLightProbeVolume {
    char m_pad[5576];
    Color m_Entity_Color; // Size: 4
    float32 m_Entity_flBrightness; // Size: 4
    void* m_Entity_hCubemapTexture;
    bool m_Entity_bCustomCubemapTexture; // Size: 8
    char m_pad7_5600[7];
    void* m_Entity_hLightProbeTexture;
    void* m_Entity_hLightProbeDirectLightIndicesTexture;
    void* m_Entity_hLightProbeDirectLightScalarsTexture;
    void* m_Entity_hLightProbeDirectLightShadowsTexture;
    Vector m_Entity_vBoxMins; // Size: 12
    Vector m_Entity_vBoxMaxs; // Size: 12
    bool m_Entity_bMoveable; // Size: 4
    char m_pad3_5660[3];
    int32 m_Entity_nHandshake; // Size: 4
    int32 m_Entity_nEnvCubeMapArrayIndex; // Size: 4
    int32 m_Entity_nPriority; // Size: 4
    bool m_Entity_bStartDisabled; // Size: 4
    char m_pad3_5676[3];
    float32 m_Entity_flEdgeFadeDist; // Size: 4
    Vector m_Entity_vEdgeFadeDists; // Size: 12
    int32 m_Entity_nLightProbeSizeX; // Size: 4
    int32 m_Entity_nLightProbeSizeY; // Size: 4
    int32 m_Entity_nLightProbeSizeZ; // Size: 4
    int32 m_Entity_nLightProbeAtlasX; // Size: 4
    int32 m_Entity_nLightProbeAtlasY; // Size: 4
    int32 m_Entity_nLightProbeAtlasZ; // Size: 25
    char m_pad21_5737[21];
};

struct __declspec(align(8)) C_EnvCubemap {
    char m_pad[1512];
    void* m_Entity_hCubemapTexture;
    bool m_Entity_bCustomCubemapTexture; // Size: 4
    char m_pad3_1524[3];
    float32 m_Entity_flInfluenceRadius; // Size: 4
    Vector m_Entity_vBoxProjectMins; // Size: 12
    Vector m_Entity_vBoxProjectMaxs; // Size: 12
    bool m_Entity_bMoveable; // Size: 4
    char m_pad3_1556[3];
    int32 m_Entity_nHandshake; // Size: 4
    int32 m_Entity_nEnvCubeMapArrayIndex; // Size: 4
    int32 m_Entity_nPriority; // Size: 4
    float32 m_Entity_flEdgeFadeDist; // Size: 4
    Vector m_Entity_vEdgeFadeDists; // Size: 12
    float32 m_Entity_flDiffuseScale; // Size: 4
    bool m_Entity_bStartDisabled; // Size: 1
    bool m_Entity_bDefaultEnvMap; // Size: 1
    bool m_Entity_bDefaultSpecEnvMap; // Size: 1
    bool m_Entity_bIndoorCubeMap; // Size: 1
    bool m_Entity_bCopyDiffuseFromDefaultCubemap; // Size: 16
    char m_pad15_1608[15];
};

struct __declspec(align(8)) C_EnvCubemapBox {
};

struct __declspec(align(8)) C_EnvCubemapFog {
    char m_pad[1384];
    float32 m_flEndDistance; // Size: 4
    float32 m_flStartDistance; // Size: 4
    float32 m_flFogFalloffExponent; // Size: 4
    bool m_bHeightFogEnabled; // Size: 4
    char m_pad3_1400[3];
    float32 m_flFogHeightWidth; // Size: 4
    float32 m_flFogHeightEnd; // Size: 4
    float32 m_flFogHeightStart; // Size: 4
    float32 m_flFogHeightExponent; // Size: 4
    float32 m_flLODBias; // Size: 4
    bool m_bActive; // Size: 1
    bool m_bStartDisabled; // Size: 3
    char m_pad2_1424[2];
    float32 m_flFogMaxOpacity; // Size: 4
    int32 m_nCubemapSourceType; // Size: 4
    void* m_hSkyMaterial;
    void* m_iszSkyEntity;
    void* m_hFogCubemapTexture;
    bool m_bHasHeightFogEnd; // Size: 1
};

struct __declspec(align(8)) C_GradientFog {
    char m_pad[1384];
    void* m_hGradientFogTexture;
    float32 m_flFogStartDistance; // Size: 4
    float32 m_flFogEndDistance; // Size: 4
    bool m_bHeightFogEnabled; // Size: 4
    char m_pad3_1404[3];
    float32 m_flFogStartHeight; // Size: 4
    float32 m_flFogEndHeight; // Size: 4
    float32 m_flFarZ; // Size: 4
    float32 m_flFogMaxOpacity; // Size: 4
    float32 m_flFogFalloffExponent; // Size: 4
    float32 m_flFogVerticalExponent; // Size: 4
    Color m_fogColor; // Size: 4
    float32 m_flFogStrength; // Size: 4
    float32 m_flFadeTime; // Size: 4
    bool m_bStartDisabled; // Size: 1
    bool m_bIsEnabled; // Size: 1
};

struct __declspec(align(8)) C_EnvLightProbeVolume {
    char m_pad[5448];
    void* m_Entity_hLightProbeTexture;
    void* m_Entity_hLightProbeDirectLightIndicesTexture;
    void* m_Entity_hLightProbeDirectLightScalarsTexture;
    void* m_Entity_hLightProbeDirectLightShadowsTexture;
    Vector m_Entity_vBoxMins; // Size: 12
    Vector m_Entity_vBoxMaxs; // Size: 12
    bool m_Entity_bMoveable; // Size: 4
    char m_pad3_5508[3];
    int32 m_Entity_nHandshake; // Size: 4
    int32 m_Entity_nPriority; // Size: 4
    bool m_Entity_bStartDisabled; // Size: 4
    char m_pad3_5520[3];
    int32 m_Entity_nLightProbeSizeX; // Size: 4
    int32 m_Entity_nLightProbeSizeY; // Size: 4
    int32 m_Entity_nLightProbeSizeZ; // Size: 4
    int32 m_Entity_nLightProbeAtlasX; // Size: 4
    int32 m_Entity_nLightProbeAtlasY; // Size: 4
    int32 m_Entity_nLightProbeAtlasZ; // Size: 13
    char m_pad9_5553[9];
};

struct __declspec(align(8)) C_PlayerVisibility {
    char m_pad[1384];
    float32 m_flVisibilityStrength; // Size: 4
    float32 m_flFogDistanceMultiplier; // Size: 4
    float32 m_flFogMaxDensityMultiplier; // Size: 4
    float32 m_flFadeTime; // Size: 4
    bool m_bStartDisabled; // Size: 1
};

struct __declspec(align(8)) C_EnvVolumetricFogController {
    char m_pad[1384];
    float32 m_flScattering; // Size: 4
    float32 m_flAnisotropy; // Size: 4
    float32 m_flFadeSpeed; // Size: 4
    float32 m_flDrawDistance; // Size: 4
    float32 m_flFadeInStart; // Size: 4
    float32 m_flFadeInEnd; // Size: 4
    float32 m_flIndirectStrength; // Size: 4
    int32 m_nVolumeDepth; // Size: 4
    float32 m_fFirstVolumeSliceThickness; // Size: 4
    int32 m_nIndirectTextureDimX; // Size: 4
    int32 m_nIndirectTextureDimY; // Size: 4
    int32 m_nIndirectTextureDimZ; // Size: 4
    Vector m_vBoxMins; // Size: 12
    Vector m_vBoxMaxs; // Size: 12
    bool m_bActive; // Size: 4
    char m_pad3_1460[3];
    char m_flStartAnisoTime[4];
    char m_flStartScatterTime[4];
    char m_flStartDrawDistanceTime[4];
    float32 m_flStartAnisotropy; // Size: 4
    float32 m_flStartScattering; // Size: 4
    float32 m_flStartDrawDistance; // Size: 4
    float32 m_flDefaultAnisotropy; // Size: 4
    float32 m_flDefaultScattering; // Size: 4
    float32 m_flDefaultDrawDistance; // Size: 4
    bool m_bStartDisabled; // Size: 1
    bool m_bEnableIndirect; // Size: 1
    bool m_bIndirectUseLPVs; // Size: 1
    bool m_bIsMaster; // Size: 5
    char m_pad4_1504[4];
    void* m_hFogIndirectTexture;
    int32 m_nForceRefreshCount; // Size: 4
    float32 m_fNoiseSpeed; // Size: 4
    float32 m_fNoiseStrength; // Size: 4
    Vector m_vNoiseScale; // Size: 12
};

struct __declspec(align(8)) C_EnvVolumetricFogVolume {
    char m_pad[1384];
    bool m_bActive; // Size: 4
    char m_pad3_1388[3];
    Vector m_vBoxMins; // Size: 12
    Vector m_vBoxMaxs; // Size: 12
    bool m_bStartDisabled; // Size: 4
    char m_pad3_1416[3];
    float32 m_flStrength; // Size: 4
    int32 m_nFalloffShape; // Size: 4
    float32 m_flFalloffExponent; // Size: 4
    float32 m_flHeightFogDepth; // Size: 4
    float32 m_fHeightFogEdgeWidth; // Size: 4
    float32 m_fIndirectLightStrength; // Size: 4
    float32 m_fSunLightStrength; // Size: 4
    float32 m_fNoiseStrength; // Size: 4
    bool m_bOverrideIndirectLightStrength; // Size: 1
    bool m_bOverrideSunLightStrength; // Size: 1
    bool m_bOverrideNoiseStrength; // Size: 1
};

struct __declspec(align(8)) CInfoTarget {
};

struct __declspec(align(8)) CInfoParticleTarget {
};

struct __declspec(align(8)) C_InfoVisibilityBox {
    char m_pad[1388];
    int32 m_nMode; // Size: 4
    Vector m_vBoxSize; // Size: 12
};

struct __declspec(align(8)) CInfoWorldLayer {
    char m_pad[1384];
    char m_pOutputOnEntitiesSpawned[40];
    void* m_worldName;
    void* m_layerName;
    bool m_bWorldLayerVisible; // Size: 1
    bool m_bEntitiesSpawned; // Size: 1
    bool m_bCreateAsChildSpawnGroup; // Size: 2
    char m_pad1_1444[1];
    uint32 m_hLayerSpawnGroup; // Size: 4
};

struct __declspec(align(8)) CPointChildModifier {
    char m_pad[1384];
};

struct __declspec(align(8)) C_PointCameraVFOV {
    char m_pad[1480];
};

struct __declspec(align(8)) CPointTemplate {
    char m_pad[1384];
    void* m_iszWorldName;
    void* m_iszSource2EntityLumpName;
    void* m_iszEntityFilterName;
    float32 m_flTimeoutInterval; // Size: 4
    bool m_bAsynchronouslySpawnEntities; // Size: 4
    char m_pad3_1416[3];
    char m_pOutputOnSpawned[40];
    char m_clientOnlyEntityBehavior[4];
    char m_ownerSpawnGroupType[4];
    char m_createdSpawnGroupHandles[24];
    char m_SpawnedEntityHandles[24];
    void* m_ScriptSpawnCallback;
};

struct __declspec(align(8)) CRagdollManager {
    char m_pad[1384];
};

struct  C_SoundAreaEntityBase {
    char m_pad[1384];
    bool m_bDisabled; // Size: 8
    char m_pad7_1392[7];
    bool m_bWasEnabled; // Size: 8
    char m_pad7_1400[7];
    void* m_iszSoundAreaType;
};

struct __declspec(align(8)) C_SoundAreaEntitySphere {
    char m_pad[1424];
};

struct __declspec(align(8)) C_SoundAreaEntityOrientedBox {
    char m_pad[1424];
    Vector m_vMin; // Size: 12
};

struct __declspec(align(8)) C_SoundEventEntity {
    char m_pad[1384];
    bool m_bStartOnSpawn; // Size: 1
    bool m_bToLocalPlayer; // Size: 1
    bool m_bStopOnNew; // Size: 1
    bool m_bSaveRestore; // Size: 1
    bool m_bSavedIsPlaying; // Size: 4
    char m_pad3_1392[3];
    float32 m_flSavedElapsedTime; // Size: 8
    char m_pad4_1400[4];
    void* m_iszSourceEntityName;
    void* m_iszAttachmentName;
    char m_onGUIDChanged[40];
    char m_onSoundFinished[40];
    float32 m_flClientCullRadius; // Size: 48
    char m_pad44_1544[44];
    char m_iszSoundName[16];
    char m_hSource[4];
};

struct __declspec(align(8)) C_SoundEventEntityAlias_snd_event_point {
};

struct __declspec(align(8)) C_SoundEventAABBEntity {
    char m_pad[1576];
    Vector m_vMins; // Size: 12
};

struct __declspec(align(8)) C_SoundEventOBBEntity {
    char m_pad[1576];
    Vector m_vMins; // Size: 12
};

struct __declspec(align(8)) C_SoundEventSphereEntity {
    char m_pad[1576];
};

struct __declspec(align(8)) C_SoundEventPathCornerEntity {
    char m_pad[1576];
};

struct __declspec(align(8)) C_BasePlayerPawn {
    char m_pad[4520];
    CPlayer_WeaponServices* m_pWeaponServices; // Size: 8
    CPlayer_ItemServices* m_pItemServices; // Size: 8
    CPlayer_AutoaimServices* m_pAutoaimServices; // Size: 8
    CPlayer_ObserverServices* m_pObserverServices; // Size: 8
    CPlayer_WaterServices* m_pWaterServices; // Size: 8
    CPlayer_UseServices* m_pUseServices; // Size: 8
    CPlayer_FlashlightServices* m_pFlashlightServices; // Size: 8
    CPlayer_CameraServices* m_pCameraServices; // Size: 8
    CPlayer_MovementServices* m_pMovementServices; // Size: 16
    char m_ServerViewAngleChanges[80];
    uint32 m_nHighestConsumedServerViewAngleChangeIndex; // Size: 4
    QAngle v_angle; // Size: 12
    QAngle v_anglePrevious; // Size: 12
    uint32 m_iHideHUD; // Size: 4
    sky3dparams_t m_skybox3d; // Size: 144
    char m_flDeathTime[4];
    Vector m_vecPredictionError; // Size: 12
    char m_flPredictionErrorTime[4];
    Vector m_vecLastCameraSetupLocalOrigin; // Size: 12
    char m_flLastCameraSetupTime[4];
    float32 m_flFOVSensitivityAdjust; // Size: 4
    float32 m_flMouseSensitivity; // Size: 4
    Vector m_vOldOrigin; // Size: 12
    float32 m_flOldSimulationTime; // Size: 4
    int32 m_nLastExecutedCommandNumber; // Size: 4
    int32 m_nLastExecutedCommandTick; // Size: 4
    char m_hController[4];
};

struct __declspec(align(8)) C_Team {
    char m_pad[1384];
    char m_aPlayerControllers[24];
    char m_aPlayers[24];
    int32 m_iScore; // Size: 4
};

struct __declspec(align(8)) CBasePlayerVData {
    char m_pad[40];
    char m_sModelName[224];
    char m_flHeadDamageMultiplier[16];
    char m_flChestDamageMultiplier[16];
    char m_flStomachDamageMultiplier[16];
    char m_flArmDamageMultiplier[16];
    char m_flLegDamageMultiplier[16];
    float32 m_flHoldBreathTime; // Size: 4
    float32 m_flDrowningDamageInterval; // Size: 4
    int32 m_nDrowningDamageInitial; // Size: 4
    int32 m_nDrowningDamageMax; // Size: 4
    int32 m_nWaterSpeed; // Size: 4
    float32 m_flUseRange; // Size: 4
    float32 m_flUseAngleTolerance; // Size: 4
};

struct __declspec(align(8)) CBasePlayerWeaponVData {
    char m_pad[40];
    char m_szWorldModel[224];
    char m_sToolsOnlyOwnerModelName[224];
    bool m_bBuiltRightHanded; // Size: 1
    bool m_bAllowFlipping; // Size: 7
    char m_pad6_496[6];
    char m_sMuzzleAttachment[32];
    char m_szMuzzleFlashParticle[224];
    bool m_bLinkedCooldowns; // Size: 1
    char m_iFlags[1];
    char m_nPrimaryAmmoType[1];
    char m_nSecondaryAmmoType[1];
    int32 m_iMaxClip1; // Size: 4
    int32 m_iMaxClip2; // Size: 4
    int32 m_iDefaultClip1; // Size: 4
    int32 m_iDefaultClip2; // Size: 4
    bool m_bReserveAmmoAsClips; // Size: 4
    char m_pad3_776[3];
    int32 m_iWeight; // Size: 4
    bool m_bAutoSwitchTo; // Size: 1
    bool m_bAutoSwitchFrom; // Size: 3
    char m_pad2_784[2];
    char m_iRumbleEffect[4];
    int32 m_iSlot; // Size: 4
    int32 m_iPosition; // Size: 8
    char m_pad4_800[4];
};

struct  CClientAlphaProperty {
    char m_pad[16];
    uint8 m_nRenderFX; // Size: 1
    char m_nReserved[19];
    uint8 m_nAlpha; // Size: 1
    uint16 m_nDesyncOffset; // Size: 2
    uint16 m_nReserved2; // Size: 2
    uint16 m_nDistFadeStart; // Size: 2
    uint16 m_nDistFadeEnd; // Size: 2
    float32 m_flFadeScale; // Size: 4
    char m_flRenderFxStartTime[4];
};

struct __declspec(align(8)) CServerOnlyModelEntity {
};

struct __declspec(align(8)) C_ModelPointEntity {
};

struct __declspec(align(8)) CLogicRelay {
    char m_pad[1384];
    char m_OnTrigger[40];
    char m_OnSpawn[40];
    bool m_bDisabled; // Size: 1
    bool m_bWaitForRefire; // Size: 1
    bool m_bTriggerOnce; // Size: 1
    bool m_bFastRetrigger; // Size: 1
};

struct __declspec(align(8)) C_ParticleSystem {
    char m_pad[3368];
    char m_szSnapshotFileName[512];
    bool m_bActive; // Size: 1
    bool m_bFrozen; // Size: 3
    char m_pad2_3884[2];
    float32 m_flFreezeTransitionDuration; // Size: 4
    int32 m_nStopType; // Size: 4
    bool m_bAnimateDuringGameplayPause; // Size: 4
    char m_pad3_3896[3];
    void* m_iEffectIndex;
    char m_flStartTime[4];
    float32 m_flPreSimTime; // Size: 4
    char m_vServerControlPoints[48];
    char m_iServerControlPointAssignments[4];
    char m_hControlPointEnts[256];
    bool m_bNoSave; // Size: 1
    bool m_bNoFreeze; // Size: 1
    bool m_bNoRamp; // Size: 1
    bool m_bStartActive; // Size: 1
    void* m_iszEffectName;
    char m_iszControlPointNames[512];
    int32 m_nDataCP; // Size: 4
    Vector m_vecDataCPValue; // Size: 12
    int32 m_nTintCP; // Size: 4
    Color m_clrTint; // Size: 36
    bool m_bOldActive; // Size: 1
};

struct __declspec(align(8)) C_PathParticleRope {
    char m_pad[1392];
    bool m_bStartActive; // Size: 4
    char m_pad3_1396[3];
    float32 m_flMaxSimulationTime; // Size: 4
    void* m_iszEffectName;
    char m_PathNodes_Name[24];
    float32 m_flParticleSpacing; // Size: 4
    float32 m_flSlack; // Size: 4
    float32 m_flRadius; // Size: 4
    Color m_ColorTint; // Size: 4
    int32 m_nEffectState; // Size: 8
    char m_pad4_1456[4];
    void* m_iEffectIndex;
    char m_PathNodes_Position[24];
    char m_PathNodes_TangentIn[24];
    char m_PathNodes_TangentOut[24];
    char m_PathNodes_Color[24];
    char m_PathNodes_PinEnabled[24];
};

struct __declspec(align(8)) C_PathParticleRopeAlias_path_particle_rope_clientside {
};

struct __declspec(align(8)) CPathSimple {
    char m_pad[1472];
};

struct __declspec(align(8)) C_DynamicLight {
    char m_pad[3368];
    uint8 m_Flags; // Size: 1
    uint8 m_LightStyle; // Size: 3
    char m_pad2_3372[2];
    float32 m_Radius; // Size: 4
    int32 m_Exponent; // Size: 4
    float32 m_InnerAngle; // Size: 4
    float32 m_OuterAngle; // Size: 4
};

struct __declspec(align(8)) C_EnvScreenOverlay {
    char m_pad[1384];
    char m_iszOverlayNames[80];
    char m_flOverlayTimes[40];
    char m_flStartTime[4];
    int32 m_iDesiredOverlay; // Size: 4
    bool m_bIsActive; // Size: 1
    bool m_bWasActive; // Size: 3
    char m_pad2_1516[2];
    int32 m_iCachedDesiredOverlay; // Size: 4
    int32 m_iCurrentOverlay; // Size: 4
};

struct __declspec(align(8)) C_FuncTrackTrain {
    char m_pad[3368];
    int32 m_nLongAxis; // Size: 4
    float32 m_flRadius; // Size: 4
};

struct  C_LightGlowOverlay {
    char m_pad[208];
    Vector m_vecOrigin; // Size: 12
    Vector m_vecDirection; // Size: 12
    int32 m_nMinDist; // Size: 4
    int32 m_nMaxDist; // Size: 4
    int32 m_nOuterMaxDist; // Size: 4
    bool m_bOneSided; // Size: 1
};

struct __declspec(align(8)) C_LightGlow {
    char m_pad[3368];
    uint32 m_nHorizontalSize; // Size: 4
    uint32 m_nVerticalSize; // Size: 4
    uint32 m_nMinDist; // Size: 4
    uint32 m_nMaxDist; // Size: 4
    uint32 m_nOuterMaxDist; // Size: 4
    float32 m_flGlowProxySize; // Size: 4
    float32 m_flHDRColorScale; // Size: 8
    char m_pad4_3400[4];
};

struct __declspec(align(8)) C_SpotlightEnd {
    char m_pad[3368];
    float32 m_flLightScale; // Size: 4
};

struct __declspec(align(8)) C_PointValueRemapper {
    char m_pad[1384];
    bool m_bDisabled; // Size: 1
    bool m_bDisabledOld; // Size: 1
    bool m_bUpdateOnClient; // Size: 2
    char m_pad1_1388[1];
    char m_nInputType[4];
    char m_hRemapLineStart[4];
    char m_hRemapLineEnd[4];
    float32 m_flMaximumChangePerSecond; // Size: 4
    float32 m_flDisengageDistance; // Size: 4
    float32 m_flEngageDistance; // Size: 4
    bool m_bRequiresUseKey; // Size: 4
    char m_pad3_1416[3];
    void* m_nOutputType;
    char m_hOutputEntities[24];
    char m_nHapticsType[4];
    char m_nMomentumType[4];
    float32 m_flMomentumModifier; // Size: 4
    float32 m_flSnapValue; // Size: 4
    float32 m_flCurrentMomentum; // Size: 4
    char m_nRatchetType[4];
    float32 m_flRatchetOffset; // Size: 4
    float32 m_flInputOffset; // Size: 4
    bool m_bEngaged; // Size: 1
    bool m_bFirstUpdate; // Size: 3
    char m_pad2_1484[2];
    float32 m_flPreviousValue; // Size: 4
    char m_flPreviousUpdateTickTime[4];
};

struct __declspec(align(8)) C_PointWorldText {
    char m_pad[3376];
    bool m_bForceRecreateNextUpdate; // Size: 16
    char m_pad15_3392[15];
    char m_messageText[512];
    char m_FontName[64];
    bool m_bEnabled; // Size: 1
    bool m_bFullbright; // Size: 3
    char m_pad2_3972[2];
    float32 m_flWorldUnitsPerPx; // Size: 4
    float32 m_flFontSize; // Size: 4
    float32 m_flDepthOffset; // Size: 4
    Color m_Color; // Size: 4
    char m_nJustifyHorizontal[4];
    char m_nJustifyVertical[4];
};

struct __declspec(align(8)) CCitadelSoundOpvarSetOBB {
    char m_pad[1408];
    void* m_iszStackName;
    void* m_iszOperatorName;
    void* m_iszOpvarName;
    Vector m_vDistanceInnerMins; // Size: 12
    Vector m_vDistanceInnerMaxs; // Size: 12
    Vector m_vDistanceOuterMins; // Size: 12
    Vector m_vDistanceOuterMaxs; // Size: 12
};

struct __declspec(align(8)) C_HandleTest {
    char m_pad[1384];
    char m_Handle[4];
};

struct __declspec(align(8)) C_EnvWind {
    char m_pad[1384];
};

struct __declspec(align(8)) C_BaseToggle {
};

struct __declspec(align(8)) C_BaseButton {
    char m_pad[3368];
    char m_glowEntity[4];
    bool m_usable; // Size: 4
    char m_pad3_3376[3];
};

struct __declspec(align(8)) C_PrecipitationBlocker {
};

struct __declspec(align(8)) C_EntityDissolve {
    char m_pad[3376];
    char m_flStartTime[4];
    float32 m_flFadeInStart; // Size: 4
    float32 m_flFadeInLength; // Size: 4
    float32 m_flFadeOutModelStart; // Size: 4
    float32 m_flFadeOutModelLength; // Size: 4
    float32 m_flFadeOutStart; // Size: 4
    float32 m_flFadeOutLength; // Size: 4
    char m_flNextSparkTime[4];
    char m_nDissolveType[4];
    Vector m_vDissolverOrigin; // Size: 12
    uint32 m_nMagnitude; // Size: 4
    bool m_bCoreExplode; // Size: 1
};

struct __declspec(align(8)) C_EnvProjectedTexture {
};

struct __declspec(align(8)) C_EnvDecal {
    char m_pad[3368];
    void* m_hDecalMaterial;
    float32 m_flWidth; // Size: 4
    float32 m_flHeight; // Size: 4
    float32 m_flDepth; // Size: 4
    uint32 m_nRenderOrder; // Size: 4
    bool m_bProjectOnWorld; // Size: 1
    bool m_bProjectOnCharacters; // Size: 1
    bool m_bProjectOnWater; // Size: 2
    char m_pad1_3396[1];
};

struct __declspec(align(8)) C_FuncBrush {
};

struct __declspec(align(8)) C_FuncElectrifiedVolume {
    char m_pad[3368];
    void* m_nAmbientEffect;
    void* m_EffectName;
};

struct __declspec(align(8)) C_FuncRotating {
};

struct __declspec(align(8)) C_Breakable {
};

struct __declspec(align(8)) C_PhysBox {
};

struct __declspec(align(8)) C_BaseFlex {
    char m_pad[3992];
    char m_flexWeight[24];
    Vector m_vLookTargetPosition; // Size: 24
    bool m_blinktoggle; // Size: 96
    char m_pad95_4136[95];
    int32 m_nLastFlexUpdateFrameCount; // Size: 4
    Vector m_CachedViewTarget; // Size: 12
    char m_nNextSceneEventId[4];
    int32 m_iBlink; // Size: 4
    float32 m_blinktime; // Size: 4
    bool m_prevblinktoggle; // Size: 4
    char m_pad3_4168[3];
    int32 m_iJawOpen; // Size: 4
    float32 m_flJawOpenAmount; // Size: 4
    float32 m_flBlinkAmount; // Size: 4
    char m_iMouthAttachment[1];
    char m_iEyeAttachment[1];
    bool m_bResetFlexWeightsOnModelChange; // Size: 26
    char m_pad25_4208[25];
    int32 m_nEyeOcclusionRendererBone; // Size: 4
    char m_mEyeOcclusionRendererCameraToBoneTransform[48];
    Vector m_vEyeOcclusionRendererHalfExtent; // Size: 28
};

struct __declspec(align(8)) C_SceneEntity {
    char m_pad[1392];
    bool m_bIsPlayingBack; // Size: 1
    bool m_bPaused; // Size: 1
    bool m_bMultiplayer; // Size: 1
    bool m_bAutogenerated; // Size: 1
    float32 m_flForceClientTime; // Size: 4
    uint16 m_nSceneStringIndex; // Size: 2
    bool m_bClientOnly; // Size: 2
    char m_pad1_1404[1];
    char m_hOwner[4];
    char m_hActorList[24];
    bool m_bWasPlaying; // Size: 16
    char m_pad15_1448[15];
    char m_QueuedEvents[24];
};

struct  C_SunGlowOverlay {
    char m_pad[208];
};

struct __declspec(align(8)) C_Sun {
    char m_pad[3368];
    char m_fxSSSunFlareEffectIndex[4];
    char m_fxSunFlareEffectIndex[4];
    float32 m_fdistNormalize; // Size: 4
    Vector m_vSunPos; // Size: 12
    Vector m_vDirection; // Size: 16
    void* m_iszEffectName;
    void* m_iszSSEffectName;
    Color m_clrOverlay; // Size: 4
    bool m_bOn; // Size: 1
    bool m_bmaxColor; // Size: 3
    char m_pad2_3432[2];
    float32 m_flSize; // Size: 4
    float32 m_flHazeScale; // Size: 4
    float32 m_flRotation; // Size: 4
    float32 m_flHDRColorScale; // Size: 4
    float32 m_flAlphaHaze; // Size: 4
    float32 m_flAlphaScale; // Size: 4
    float32 m_flAlphaHdr; // Size: 4
};

struct __declspec(align(8)) C_BaseTrigger {
    char m_pad[3368];
    bool m_bDisabled; // Size: 1
};

struct __declspec(align(8)) C_TriggerVolume {
};

struct __declspec(align(8)) C_TriggerMultiple {
};

struct __declspec(align(8)) C_TriggerLerpObject {
};

struct __declspec(align(8)) C_TriggerPhysics {
    char m_pad[3376];
    float32 m_gravityScale; // Size: 4
    float32 m_linearLimit; // Size: 4
    float32 m_linearDamping; // Size: 4
    float32 m_angularLimit; // Size: 4
    float32 m_angularDamping; // Size: 4
    float32 m_linearForce; // Size: 4
    float32 m_flFrequency; // Size: 4
    float32 m_flDampingRatio; // Size: 4
    Vector m_vecLinearForcePointAt; // Size: 12
    bool m_bCollapseToForcePoint; // Size: 4
    char m_pad3_3424[3];
    Vector m_vecLinearForcePointAtWorld; // Size: 12
    Vector m_vecLinearForceDirection; // Size: 12
};

struct __declspec(align(8)) C_Beam {
    char m_pad[3368];
    float32 m_flFrameRate; // Size: 4
    float32 m_flHDRColorScale; // Size: 4
    char m_flFireTime[4];
    float32 m_flDamage; // Size: 4
    uint8 m_nNumBeamEnts; // Size: 4
    char m_pad3_3388[3];
    int32 m_queryHandleHalo; // Size: 36
    char m_pad32_3424[32];
    void* m_hBaseMaterial;
    void* m_nHaloIndex;
    char m_nBeamType[4];
    uint32 m_nBeamFlags; // Size: 4
    char m_hAttachEntity[40];
    char m_nAttachIndex[12];
    float32 m_fWidth; // Size: 4
    float32 m_fEndWidth; // Size: 4
    float32 m_fFadeLength; // Size: 4
    float32 m_fHaloScale; // Size: 4
    float32 m_fAmplitude; // Size: 4
    float32 m_fStartFrame; // Size: 4
    float32 m_fSpeed; // Size: 4
    float32 m_flFrame; // Size: 4
    char m_nClipStyle[4];
    bool m_bTurnedOff; // Size: 4
    char m_pad3_3540[3];
    Vector m_vecEndPos; // Size: 12
};

struct __declspec(align(8)) C_FuncLadder {
    char m_pad[3368];
    Vector m_vecLadderDir; // Size: 16
    char m_Dismounts[24];
    Vector m_vecLocalTop; // Size: 12
    Vector m_vecPlayerMountPositionTop; // Size: 12
    Vector m_vecPlayerMountPositionBottom; // Size: 12
    float32 m_flAutoRideSpeed; // Size: 4
    bool m_bDisabled; // Size: 1
    bool m_bFakeLadder; // Size: 1
};

struct __declspec(align(8)) CPrecipitationVData {
    char m_pad[40];
    char m_szParticlePrecipitationEffect[224];
    float32 m_flInnerDistance; // Size: 4
    char m_nAttachType[4];
    bool m_bBatchSameVolumeType; // Size: 4
    char m_pad3_276[3];
    int32 m_nRTEnvCP; // Size: 4
    int32 m_nRTEnvCPComponent; // Size: 8
    char m_pad4_288[4];
};

struct __declspec(align(8)) C_Sprite {
    char m_pad[3368];
    void* m_hSpriteMaterial;
    char m_hAttachedToEntity[4];
    char m_nAttachment[4];
    float32 m_flSpriteFramerate; // Size: 4
    float32 m_flFrame; // Size: 4
    char m_flDieTime[16];
    uint32 m_nBrightness; // Size: 4
    float32 m_flBrightnessDuration; // Size: 4
    float32 m_flSpriteScale; // Size: 4
    float32 m_flScaleDuration; // Size: 4
    bool m_bWorldSpaceScale; // Size: 4
    char m_pad3_3428[3];
    float32 m_flGlowProxySize; // Size: 4
    float32 m_flHDRColorScale; // Size: 4
    char m_flLastTime[4];
    float32 m_flMaxFrame; // Size: 4
    float32 m_flStartScale; // Size: 4
    float32 m_flDestScale; // Size: 4
    char m_flScaleTimeStart[4];
    int32 m_nStartBrightness; // Size: 4
    int32 m_nDestBrightness; // Size: 4
    void* m_flBrightnessTimeStart;
    char m_hOldSpriteMaterial[160];
    int32 m_nSpriteWidth; // Size: 4
};

struct __declspec(align(8)) CSpriteOriented {
};

struct  C_BaseClientUIEntity {
    char m_pad[3376];
    bool m_bEnabled; // Size: 8
    char m_pad7_3384[7];
    void* m_DialogXMLName;
    void* m_PanelClassName;
};

struct __declspec(align(8)) C_PointClientUIDialog {
    char m_pad[3416];
    char m_hActivator[4];
};

struct __declspec(align(8)) C_PointClientUIHUD {
    char m_pad[3424];
    bool m_bCheckCSSClasses; // Size: 384
    char m_pad383_3808[383];
    bool m_bIgnoreInput; // Size: 4
    char m_pad3_3812[3];
    float32 m_flWidth; // Size: 4
    float32 m_flHeight; // Size: 4
    float32 m_flDPI; // Size: 4
    float32 m_flInteractDistance; // Size: 4
    float32 m_flDepthOffset; // Size: 4
    uint32 m_unOwnerContext; // Size: 4
    uint32 m_unHorizontalAlign; // Size: 4
    uint32 m_unVerticalAlign; // Size: 4
    uint32 m_unOrientation; // Size: 4
    bool m_bAllowInteractionFromAllSceneWorlds; // Size: 8
    char m_pad7_3856[7];
};

struct __declspec(align(16)) CPointOffScreenIndicatorUi {
    char m_pad[3984];
    bool m_bBeenEnabled; // Size: 1
    bool m_bHide; // Size: 3
    char m_pad2_3988[2];
    float32 m_flSeenTargetTime; // Size: 4
};

struct __declspec(align(16)) C_PointClientUIWorldPanel {
    char m_pad[3424];
    bool m_bForceRecreateNextUpdate; // Size: 1
    bool m_bMoveViewToPlayerNextThink; // Size: 1
    bool m_bCheckCSSClasses; // Size: 14
    char m_pad13_3440[13];
    char m_anchorDeltaTransform[408];
    CPointOffScreenIndicatorUi* m_pOffScreenIndicator; // Size: 40
    bool m_bIgnoreInput; // Size: 1
    bool m_bLit; // Size: 1
    bool m_bFollowPlayerAcrossTeleport; // Size: 2
    char m_pad1_3892[1];
    float32 m_flWidth; // Size: 4
    float32 m_flHeight; // Size: 4
    float32 m_flDPI; // Size: 4
    float32 m_flInteractDistance; // Size: 4
    float32 m_flDepthOffset; // Size: 4
    uint32 m_unOwnerContext; // Size: 4
    uint32 m_unHorizontalAlign; // Size: 4
    uint32 m_unVerticalAlign; // Size: 4
    uint32 m_unOrientation; // Size: 4
    bool m_bAllowInteractionFromAllSceneWorlds; // Size: 8
    char m_pad7_3936[7];
    char m_vecCSSClasses[24];
    bool m_bOpaque; // Size: 1
    bool m_bNoDepth; // Size: 1
    bool m_bRenderBackface; // Size: 1
    bool m_bUseOffScreenIndicator; // Size: 1
    bool m_bExcludeFromSaveGames; // Size: 1
    bool m_bGrabbable; // Size: 1
    bool m_bOnlyRenderToTexture; // Size: 1
    bool m_bDisableMipGen; // Size: 1
};

struct __declspec(align(16)) C_PointClientUIWorldTextPanel {
    char m_pad[3984];
};

struct __declspec(align(8)) CInfoOffscreenPanoramaTexture {
    char m_pad[1384];
    bool m_bDisabled; // Size: 4
    char m_pad3_1388[3];
    int32 m_nResolutionX; // Size: 4
    int32 m_nResolutionY; // Size: 8
    char m_pad4_1400[4];
    void* m_szLayoutFileName;
    void* m_RenderAttrName;
    char m_TargetEntities[24];
    int32 m_nTargetChangeCount; // Size: 8
    char m_pad4_1448[4];
    char m_vecCSSClasses[376];
};

struct __declspec(align(8)) CBombTarget {
    char m_pad[3376];
};

struct __declspec(align(8)) CHostageRescueZoneShim {
};

struct __declspec(align(8)) CHostageRescueZone {
};

struct __declspec(align(8)) C_TriggerBuoyancy {
    char m_pad[3376];
    CBuoyancyHelper m_BuoyancyHelper; // Size: 128
};

struct __declspec(align(8)) CFuncWater {
    char m_pad[3368];
};

struct __declspec(align(8)) CWaterSplasher {
};

struct __declspec(align(8)) C_InfoInstructorHintHostageRescueZone {
};

struct __declspec(align(8)) C_CSObserverPawn {
    char m_pad[5392];
};

struct __declspec(align(8)) C_FootstepControl {
    char m_pad[3376];
    void* m_source;
};

struct __declspec(align(8)) CCSWeaponBaseVData {
    char m_pad[840];
    char m_WeaponType[4];
    char m_WeaponCategory[4];
    char m_szViewModel[224];
    char m_szPlayerModel[224];
    char m_szWorldDroppedModel[224];
    char m_szAimsightLensMaskModel[224];
    char m_szMagazineModel[224];
    char m_szHeatEffect[224];
    char m_szEjectBrassEffect[224];
    char m_szMuzzleFlashParticleAlt[224];
    char m_szMuzzleFlashThirdPersonParticle[224];
    char m_szMuzzleFlashThirdPersonParticleAlt[224];
    char m_szTracerParticle[224];
    char m_GearSlot[4];
    int32 m_GearSlotPosition; // Size: 4
    void* m_DefaultLoadoutSlot;
    void* m_sWrongTeamMsg;
    int32 m_nPrice; // Size: 4
    int32 m_nKillAward; // Size: 4
    int32 m_nPrimaryReserveAmmoMax; // Size: 4
    int32 m_nSecondaryReserveAmmoMax; // Size: 4
    bool m_bMeleeWeapon; // Size: 1
    bool m_bHasBurstMode; // Size: 1
    bool m_bIsRevolver; // Size: 1
    bool m_bCannotShootUnderwater; // Size: 5
    char m_pad4_3360[4];
    void* m_szName;
    void* m_szAnimExtension;
    char m_eSilencerType[4];
    int32 m_nCrosshairMinDistance; // Size: 4
    int32 m_nCrosshairDeltaDistance; // Size: 4
    bool m_bIsFullAuto; // Size: 4
    char m_pad3_3392[3];
    int32 m_nNumBullets; // Size: 4
    void* m_flCycleTime;
    void* m_flMaxSpeed;
    void* m_flSpread;
    void* m_flInaccuracyCrouch;
    void* m_flInaccuracyStand;
    void* m_flInaccuracyJump;
    void* m_flInaccuracyLand;
    void* m_flInaccuracyLadder;
    void* m_flInaccuracyFire;
    void* m_flInaccuracyMove;
    void* m_flRecoilAngle;
    void* m_flRecoilAngleVariance;
    void* m_flRecoilMagnitude;
    void* m_flRecoilMagnitudeVariance;
    void* m_nTracerFrequency;
    float32 m_flInaccuracyJumpInitial; // Size: 4
    float32 m_flInaccuracyJumpApex; // Size: 4
    float32 m_flInaccuracyReload; // Size: 4
    int32 m_nRecoilSeed; // Size: 4
    int32 m_nSpreadSeed; // Size: 4
    float32 m_flTimeToIdleAfterFire; // Size: 4
    float32 m_flIdleInterval; // Size: 4
    float32 m_flAttackMovespeedFactor; // Size: 4
    float32 m_flHeatPerShot; // Size: 4
    float32 m_flInaccuracyPitchShift; // Size: 4
    float32 m_flInaccuracyAltSoundThreshold; // Size: 4
    float32 m_flBotAudibleRange; // Size: 8
    char m_pad4_3568[4];
    void* m_szUseRadioSubtitle;
    bool m_bUnzoomsAfterShot; // Size: 1
    bool m_bHideViewModelWhenZoomed; // Size: 3
    char m_pad2_3580[2];
    int32 m_nZoomLevels; // Size: 4
    int32 m_nZoomFOV1; // Size: 4
    int32 m_nZoomFOV2; // Size: 4
    float32 m_flZoomTime0; // Size: 4
    float32 m_flZoomTime1; // Size: 4
    float32 m_flZoomTime2; // Size: 4
    float32 m_flIronSightPullUpSpeed; // Size: 4
    float32 m_flIronSightPutDownSpeed; // Size: 4
    float32 m_flIronSightFOV; // Size: 4
    float32 m_flIronSightPivotForward; // Size: 4
    float32 m_flIronSightLooseness; // Size: 4
    QAngle m_angPivotAngle; // Size: 12
    Vector m_vecIronSightEyePos; // Size: 12
    int32 m_nDamage; // Size: 4
    float32 m_flHeadshotMultiplier; // Size: 4
    float32 m_flArmorRatio; // Size: 4
    float32 m_flPenetration; // Size: 4
    float32 m_flRange; // Size: 4
    float32 m_flRangeModifier; // Size: 4
    float32 m_flFlinchVelocityModifierLarge; // Size: 4
    float32 m_flFlinchVelocityModifierSmall; // Size: 4
    float32 m_flRecoveryTimeCrouch; // Size: 4
    float32 m_flRecoveryTimeStand; // Size: 4
    float32 m_flRecoveryTimeCrouchFinal; // Size: 4
    float32 m_flRecoveryTimeStandFinal; // Size: 4
    int32 m_nRecoveryTransitionStartBullet; // Size: 4
    int32 m_nRecoveryTransitionEndBullet; // Size: 4
    float32 m_flThrowVelocity; // Size: 4
    Vector m_vSmokeColor; // Size: 12
};

struct __declspec(align(8)) C_PlayerSprayDecal {
    char m_pad[3368];
    int32 m_nUniqueID; // Size: 4
    uint32 m_unAccountID; // Size: 4
    uint32 m_unTraceID; // Size: 4
    uint32 m_rtGcTime; // Size: 4
    Vector m_vecEndPos; // Size: 12
    Vector m_vecStart; // Size: 12
    Vector m_vecLeft; // Size: 12
    Vector m_vecNormal; // Size: 12
    int32 m_nPlayer; // Size: 4
    int32 m_nEntity; // Size: 4
    int32 m_nHitbox; // Size: 4
    float32 m_flCreationTime; // Size: 4
    int32 m_nTintID; // Size: 4
    uint8 m_nVersion; // Size: 1
    char m_ubSignature[139];
};

struct __declspec(align(8)) C_FuncConveyor {
    char m_pad[3376];
    Vector m_vecMoveDirEntitySpace; // Size: 12
    float32 m_flTargetSpeed; // Size: 4
    char m_nTransitionStartTick[4];
    int32 m_nTransitionDurationTicks; // Size: 4
    float32 m_flTransitionStartSpeed; // Size: 8
    char m_pad4_3408[4];
    char m_hConveyorModels[24];
    float32 m_flCurrentConveyorOffset; // Size: 4
};

struct __declspec(align(16)) CGrenadeTracer {
    char m_pad[3392];
    float32 m_flTracerDuration; // Size: 4
};

struct __declspec(align(16)) C_Inferno {
    char m_pad[3432];
    void* m_nfxFireDamageEffect;
    void* m_hInfernoPointsSnapshot;
    void* m_hInfernoFillerPointsSnapshot;
    void* m_hInfernoOutlinePointsSnapshot;
    void* m_hInfernoClimbingOutlinePointsSnapshot;
    void* m_hInfernoDecalsSnapshot;
    char m_firePositions[768];
    char m_fireParentPositions[768];
    char m_bFireIsBurning[64];
    char m_BurnNormal[768];
    int32 m_fireCount; // Size: 4
    int32 m_nInfernoType; // Size: 4
    float32 m_nFireLifetime; // Size: 4
    bool m_bInPostEffectTime; // Size: 4
    char m_pad3_5864[3];
    int32 m_lastFireCount; // Size: 4
    int32 m_nFireEffectTickBegin; // Size: 27652
    char m_pad27648_33520[27648];
    int32 m_drawableCount; // Size: 4
    bool m_blosCheck; // Size: 4
    char m_pad3_33528[3];
    int32 m_nlosperiod; // Size: 4
    float32 m_maxFireHalfWidth; // Size: 4
    float32 m_maxFireHeight; // Size: 4
    Vector m_minBounds; // Size: 12
    Vector m_maxBounds; // Size: 12
};

struct __declspec(align(16)) C_FireCrackerBlast {
};

struct __declspec(align(8)) C_BarnLight {
    char m_pad[3368];
    bool m_bEnabled; // Size: 4
    char m_pad3_3372[3];
    int32 m_nColorMode; // Size: 4
    Color m_Color; // Size: 4
    float32 m_flColorTemperature; // Size: 4
    float32 m_flBrightness; // Size: 4
    float32 m_flBrightnessScale; // Size: 4
    int32 m_nDirectLight; // Size: 4
    int32 m_nBakedShadowIndex; // Size: 4
    int32 m_nLuminaireShape; // Size: 4
    float32 m_flLuminaireSize; // Size: 4
    float32 m_flLuminaireAnisotropy; // Size: 8
    char m_pad4_3416[4];
    void* m_LightStyleString;
    void* m_flLightStyleStartTime;
    char m_QueuedLightStyleStrings[24];
    char m_LightStyleEvents[24];
    char m_LightStyleTargets[24];
    char m_StyleEvent[160];
    void* m_hLightCookie;
    float32 m_flShape; // Size: 4
    float32 m_flSoftX; // Size: 4
    float32 m_flSoftY; // Size: 4
    float32 m_flSkirt; // Size: 4
    float32 m_flSkirtNear; // Size: 4
    Vector m_vSizeParams; // Size: 12
    float32 m_flRange; // Size: 4
    Vector m_vShear; // Size: 12
    int32 m_nBakeSpecularToCubemaps; // Size: 4
    Vector m_vBakeSpecularToCubemapsSize; // Size: 12
    int32 m_nCastShadows; // Size: 4
    int32 m_nShadowMapSize; // Size: 4
    int32 m_nShadowPriority; // Size: 4
    bool m_bContactShadow; // Size: 4
    char m_pad3_3752[3];
    int32 m_nBounceLight; // Size: 4
    float32 m_flBounceScale; // Size: 4
    float32 m_flMinRoughness; // Size: 4
    Vector m_vAlternateColor; // Size: 12
    float32 m_fAlternateColorBrightness; // Size: 4
    int32 m_nFog; // Size: 4
    float32 m_flFogStrength; // Size: 4
    int32 m_nFogShadows; // Size: 4
    float32 m_flFogScale; // Size: 4
    bool m_bFogMixedShadows; // Size: 4
    char m_pad3_3800[3];
    float32 m_flFadeSizeStart; // Size: 4
    float32 m_flFadeSizeEnd; // Size: 4
    float32 m_flShadowFadeSizeStart; // Size: 4
    float32 m_flShadowFadeSizeEnd; // Size: 4
    bool m_bPrecomputedFieldsValid; // Size: 4
    char m_pad3_3820[3];
    Vector m_vPrecomputedBoundsMins; // Size: 12
    Vector m_vPrecomputedBoundsMaxs; // Size: 12
    Vector m_vPrecomputedOBBOrigin; // Size: 12
    QAngle m_vPrecomputedOBBAngles; // Size: 12
    Vector m_vPrecomputedOBBExtent; // Size: 12
    int32 m_nPrecomputedSubFrusta; // Size: 4
    Vector m_vPrecomputedOBBOrigin0; // Size: 12
    QAngle m_vPrecomputedOBBAngles0; // Size: 12
    Vector m_vPrecomputedOBBExtent0; // Size: 12
    Vector m_vPrecomputedOBBOrigin1; // Size: 12
    QAngle m_vPrecomputedOBBAngles1; // Size: 12
    Vector m_vPrecomputedOBBExtent1; // Size: 12
    Vector m_vPrecomputedOBBOrigin2; // Size: 12
    QAngle m_vPrecomputedOBBAngles2; // Size: 12
    Vector m_vPrecomputedOBBExtent2; // Size: 12
    Vector m_vPrecomputedOBBOrigin3; // Size: 12
    QAngle m_vPrecomputedOBBAngles3; // Size: 12
    Vector m_vPrecomputedOBBExtent3; // Size: 12
    Vector m_vPrecomputedOBBOrigin4; // Size: 12
    QAngle m_vPrecomputedOBBAngles4; // Size: 12
    Vector m_vPrecomputedOBBExtent4; // Size: 12
    Vector m_vPrecomputedOBBOrigin5; // Size: 12
    QAngle m_vPrecomputedOBBAngles5; // Size: 12
    Vector m_vPrecomputedOBBExtent5; // Size: 80
    bool m_bInitialBoneSetup; // Size: 8
    char m_pad7_4176[7];
};

struct __declspec(align(8)) C_RectLight {
    char m_pad[4208];
};

struct __declspec(align(8)) C_OmniLight {
    char m_pad[4208];
    float32 m_flInnerAngle; // Size: 4
    float32 m_flOuterAngle; // Size: 4
};

struct __declspec(align(8)) C_CSTeam {
    char m_pad[1568];
    char m_szTeamMatchStat[512];
    int32 m_numMapVictories; // Size: 4
    bool m_bSurrendered; // Size: 4
    char m_pad3_2088[3];
    int32 m_scoreFirstHalf; // Size: 4
    int32 m_scoreSecondHalf; // Size: 4
    int32 m_scoreOvertime; // Size: 4
    char m_szClanTeamname[132];
    uint32 m_iClanID; // Size: 4
    void* m_szTeamFlagImage;
};

struct __declspec(align(8)) C_MapPreviewParticleSystem {
};

struct __declspec(align(8)) CInfoDynamicShadowHint {
    char m_pad[1384];
    bool m_bDisabled; // Size: 4
    char m_pad3_1388[3];
    float32 m_flRange; // Size: 4
    int32 m_nImportance; // Size: 4
    int32 m_nLightChoice; // Size: 4
};

struct __declspec(align(8)) CInfoDynamicShadowHintBox {
    char m_pad[1408];
    Vector m_vBoxMins; // Size: 12
};

struct __declspec(align(8)) C_EnvSky {
    char m_pad[3368];
    void* m_hSkyMaterial;
    void* m_hSkyMaterialLightingOnly;
    bool m_bStartDisabled; // Size: 1
    Color m_vTintColor; // Size: 4
    Color m_vTintColorLightingOnly; // Size: 7
    float32 m_flBrightnessScale; // Size: 4
    int32 m_nFogType; // Size: 4
    float32 m_flFogMinStart; // Size: 4
    float32 m_flFogMinEnd; // Size: 4
    float32 m_flFogMaxStart; // Size: 4
    float32 m_flFogMaxEnd; // Size: 4
};

struct __declspec(align(8)) C_TonemapController2Alias_env_tonemap_controller2 {
};

struct __declspec(align(8)) C_LightEntity {
    char m_pad[3368];
};

struct __declspec(align(8)) C_LightSpotEntity {
};

struct __declspec(align(8)) C_LightOrthoEntity {
};

struct __declspec(align(8)) C_LightDirectionalEntity {
};

struct __declspec(align(8)) C_LightEnvironmentEntity {
};

struct __declspec(align(8)) C_EnvParticleGlow {
    char m_pad[4824];
    float32 m_flAlphaScale; // Size: 4
    float32 m_flRadiusScale; // Size: 4
    float32 m_flSelfIllumScale; // Size: 4
    Color m_ColorTint; // Size: 4
};

struct __declspec(align(8)) C_TextureBasedAnimatable {
    char m_pad[3368];
    bool m_bLoop; // Size: 4
    char m_pad3_3372[3];
    float32 m_flFPS; // Size: 4
    void* m_hPositionKeys;
    void* m_hRotationKeys;
    Vector m_vAnimationBoundsMin; // Size: 12
    Vector m_vAnimationBoundsMax; // Size: 12
    float32 m_flStartTime; // Size: 4
};

struct __declspec(align(8)) C_World {
};

struct __declspec(align(8)) CBaseProp {
    char m_pad[3976];
    bool m_bModelOverrodeBlockLOS; // Size: 4
    char m_pad3_3980[3];
    int32 m_iShapeType; // Size: 4
    bool m_bConformToCollisionBounds; // Size: 4
    char m_pad3_3988[3];
};

struct __declspec(align(8)) C_BreakableProp {
    char m_pad[4040];
    CPropDataComponent m_CPropDataComponent; // Size: 64
    char m_OnBreak[40];
    char m_OnHealthChanged[40];
    char m_OnTakeDamage[40];
    float32 m_impactEnergyScale; // Size: 4
    int32 m_iMinHealthDmg; // Size: 4
    float32 m_flPressureDelay; // Size: 4
    float32 m_flDefBurstScale; // Size: 4
    Vector m_vDefBurstOffset; // Size: 12
    char m_hBreaker[4];
    char m_PerformanceMode[4];
    char m_flPreventDamageBeforeTime[4];
    void* m_BreakableContentsType;
    void* m_strBreakableContentsPropGroupOverride;
    void* m_strBreakableContentsParticleOverride;
    bool m_bHasBreakPiecesOrCommands; // Size: 4
    char m_pad3_4292[3];
    float32 m_explodeDamage; // Size: 4
    float32 m_explodeRadius; // Size: 8
    char m_pad4_4304[4];
    float32 m_explosionDelay; // Size: 8
    char m_pad4_4312[4];
    void* m_explosionBuildupSound;
    void* m_explosionCustomEffect;
    void* m_explosionCustomSound;
    void* m_explosionModifier;
    char m_hPhysicsAttacker[4];
    char m_flLastPhysicsInfluenceTime[4];
    float32 m_flDefaultFadeScale; // Size: 4
    char m_hLastAttacker[4];
    char m_hFlareEnt[4];
};

struct __declspec(align(8)) C_DynamicProp {
    char m_pad[4368];
    bool m_bUseHitboxesForRenderBox; // Size: 1
    bool m_bUseAnimGraph; // Size: 7
    char m_pad6_4376[6];
    char m_pOutputAnimBegun[40];
    char m_pOutputAnimOver[40];
    char m_pOutputAnimLoopCycleOver[40];
    char m_OnAnimReachedStart[40];
    char m_OnAnimReachedEnd[40];
    void* m_iszIdleAnim;
    char m_nIdleAnimLoopMode[4];
    bool m_bRandomizeCycle; // Size: 1
    bool m_bStartDisabled; // Size: 1
    bool m_bFiredStartEndOutput; // Size: 1
    bool m_bForceNpcExclude; // Size: 1
    bool m_bCreateNonSolid; // Size: 1
    bool m_bIsOverrideProp; // Size: 3
    char m_pad2_4596[2];
    int32 m_iInitialGlowState; // Size: 4
    int32 m_nGlowRange; // Size: 4
    int32 m_nGlowRangeMin; // Size: 4
    Color m_glowColor; // Size: 4
    int32 m_nGlowTeam; // Size: 4
    int32 m_iCachedFrameCount; // Size: 4
    Vector m_vecCachedRenderMins; // Size: 12
};

struct __declspec(align(8)) C_DynamicPropAlias_dynamic_prop {
};

struct __declspec(align(8)) C_DynamicPropAlias_prop_dynamic_override {
};

struct __declspec(align(8)) C_DynamicPropAlias_cable_dynamic {
};

struct __declspec(align(8)) C_ColorCorrectionVolume {
    char m_pad[3376];
    float32 m_LastEnterWeight; // Size: 4
    float32 m_LastEnterTime; // Size: 4
    float32 m_LastExitWeight; // Size: 4
    float32 m_LastExitTime; // Size: 4
    bool m_bEnabled; // Size: 4
    char m_pad3_3396[3];
    float32 m_MaxWeight; // Size: 4
    float32 m_FadeDuration; // Size: 4
    float32 m_Weight; // Size: 4
};

struct __declspec(align(16)) C_FuncMonitor {
    char m_pad[3368];
    void* m_targetCamera;
    int32 m_nResolutionEnum; // Size: 4
    bool m_bRenderShadows; // Size: 1
    bool m_bUseUniqueColorTarget; // Size: 3
    char m_pad2_3384[2];
    void* m_brushModelName;
    char m_hTargetCamera[4];
    bool m_bEnabled; // Size: 1
};

struct __declspec(align(8)) C_FuncMoveLinear {
};

struct __declspec(align(8)) C_FuncMover {
};

struct __declspec(align(8)) C_PhysMagnet {
    char m_pad[3976];
    char m_aAttachedObjectsFromServer[24];
};

struct __declspec(align(8)) C_PointCommentaryNode {
    char m_pad[3984];
    bool m_bActive; // Size: 1
    bool m_bWasActive; // Size: 3
    char m_pad2_3988[2];
    char m_flEndTime[4];
    char m_flStartTime[4];
    float32 m_flStartTimeInCommentary; // Size: 4
    void* m_iszCommentaryFile;
    void* m_iszTitle;
    void* m_iszSpeakers;
    int32 m_iNodeNumber; // Size: 4
    int32 m_iNodeNumberMax; // Size: 4
    bool m_bListenedTo; // Size: 16
    char m_pad15_4048[15];
    char m_hViewPosition[4];
};

struct __declspec(align(8)) C_WaterBullet {
};

struct __declspec(align(8)) C_BaseDoor {
    char m_pad[3368];
};

struct __declspec(align(8)) C_ClientRagdoll {
    char m_pad[3976];
    bool m_bFadeOut; // Size: 1
    bool m_bImportant; // Size: 3
    char m_pad2_3980[2];
    char m_flEffectTime[4];
    char m_gibDespawnTime[4];
    int32 m_iCurrentFriction; // Size: 4
    int32 m_iMinFriction; // Size: 4
    int32 m_iMaxFriction; // Size: 4
    int32 m_iFrictionAnimState; // Size: 4
    bool m_bReleaseRagdoll; // Size: 1
    char m_iEyeAttachment[1];
    bool m_bFadingOut; // Size: 2
    char m_pad1_4008[1];
    char m_flScaleEnd[40];
    char m_flScaleTimeStart[40];
};

struct __declspec(align(8)) C_Precipitation {
    char m_pad[3376];
    float32 m_flDensity; // Size: 16
    char m_pad12_3392[12];
    float32 m_flParticleInnerDist; // Size: 8
    char m_pad4_3400[4];
    char* m_pParticleDef; // Size: 40
    void* m_tParticlePrecipTraceTimer;
    char m_bActiveParticlePrecipEmitter[1];
    bool m_bParticlePrecipInitialized; // Size: 1
    bool m_bHasSimulatedSinceLastSceneObjectUpdate; // Size: 2
    char m_pad1_3452[1];
};

struct __declspec(align(8)) C_FireSprite {
    char m_pad[3640];
    Vector m_vecMoveDir; // Size: 12
};

struct __declspec(align(8)) C_FireFromAboveSprite {
};

struct __declspec(align(8)) C_Fish {
    char m_pad[3976];
    Vector m_pos; // Size: 12
    Vector m_vel; // Size: 12
    QAngle m_angles; // Size: 12
    int32 m_localLifeState; // Size: 4
    float32 m_deathDepth; // Size: 4
    float32 m_deathAngle; // Size: 4
    float32 m_buoyancy; // Size: 8
    char m_pad4_4032[4];
    CountdownTimer m_wiggleTimer; // Size: 24
    float32 m_wigglePhase; // Size: 4
    float32 m_wiggleRate; // Size: 4
    Vector m_actualPos; // Size: 12
    QAngle m_actualAngles; // Size: 12
    Vector m_poolOrigin; // Size: 12
    float32 m_waterLevel; // Size: 4
    bool m_gotUpdate; // Size: 4
    char m_pad3_4108[3];
    float32 m_x; // Size: 4
    float32 m_y; // Size: 4
    float32 m_z; // Size: 4
    float32 m_angle; // Size: 4
    char m_errorHistory[80];
    int32 m_errorHistoryIndex; // Size: 4
    int32 m_errorHistoryCount; // Size: 4
};

struct __declspec(align(8)) C_PhysicsProp {
    char m_pad[4368];
};

struct __declspec(align(8)) C_BasePropDoor {
    char m_pad[4664];
    char m_eDoorState[4];
    bool m_modelChanged; // Size: 1
    bool m_bLocked; // Size: 3
    char m_pad2_4672[2];
    Vector m_closedPosition; // Size: 12
    QAngle m_closedAngles; // Size: 12
    char m_hMaster[4];
};

struct __declspec(align(8)) C_PropDoorRotating {
};

struct __declspec(align(8)) C_PhysPropClientside {
    char m_pad[4368];
    char m_flTouchDelta[4];
    char m_fDeathTime[4];
    float32 m_inertiaScale; // Size: 4
    Vector m_vecDamagePosition; // Size: 12
    Vector m_vecDamageDirection; // Size: 12
};

struct __declspec(align(8)) C_RagdollProp {
    char m_pad[3984];
    char m_ragPos[24];
    char m_ragAngles[24];
    float32 m_flBlendWeight; // Size: 4
    char m_hRagdollSource[4];
    char m_iEyeAttachment[4];
    float32 m_flBlendWeightCurrent; // Size: 4
    char m_parentPhysicsBoneIndices[24];
};

struct __declspec(align(8)) C_LocalTempEntity {
    char m_pad[3976];
    int32 flags; // Size: 4
    char die[4];
    float32 m_flFrameMax; // Size: 4
    float32 x; // Size: 4
    float32 y; // Size: 4
    float32 fadeSpeed; // Size: 4
    float32 bounceFactor; // Size: 4
    int32 hitSound; // Size: 4
    int32 priority; // Size: 4
    Vector tentOffset; // Size: 12
    QAngle m_vecTempEntAngVelocity; // Size: 12
    int32 tempent_renderamt; // Size: 4
    Vector m_vecNormal; // Size: 12
    float32 m_flSpriteScale; // Size: 4
    int32 m_nFlickerFrame; // Size: 4
    float32 m_flFrameRate; // Size: 4
    float32 m_flFrame; // Size: 8
    char m_pad4_4072[4];
    char* m_pszImpactEffect; // Size: 8
    char* m_pszParticleEffect; // Size: 8
    bool m_bParticleCollision; // Size: 4
    char m_pad3_4092[3];
    int32 m_iLastCollisionFrame; // Size: 4
    Vector m_vLastCollisionOrigin; // Size: 12
    Vector m_vecTempEntVelocity; // Size: 12
    Vector m_vecPrevAbsOrigin; // Size: 12
};

struct __declspec(align(8)) C_ShatterGlassShardPhysics {
    char m_pad[4384];
};

struct __declspec(align(8)) C_EconEntity {
    char m_pad[4400];
    float32 m_flFlexDelayTime; // Size: 8
    char m_pad4_4408[4];
    float32* m_flFlexDelayedWeight; // Size: 8
    bool m_bAttributesInitialized; // Size: 8
    char m_pad7_4424[7];
    C_AttributeContainer m_AttributeManager; // Size: 1192
    uint32 m_OriginalOwnerXuidLow; // Size: 4
    uint32 m_OriginalOwnerXuidHigh; // Size: 4
    int32 m_nFallbackPaintKit; // Size: 4
    int32 m_nFallbackSeed; // Size: 4
    float32 m_flFallbackWear; // Size: 4
    int32 m_nFallbackStatTrak; // Size: 4
    bool m_bClientside; // Size: 1
    bool m_bParticleSystemsCreated; // Size: 7
    char m_pad6_5648[6];
    char m_vecAttachedParticles[24];
    char m_hViewmodelAttachment[4];
    int32 m_iOldTeam; // Size: 4
    bool m_bAttachmentDirty; // Size: 4
    char m_pad3_5684[3];
    int32 m_nUnloadedModelIndex; // Size: 4
    int32 m_iNumOwnerValidationRetries; // Size: 16
    char m_pad12_5704[12];
    void* m_hOldProvidee;
};

struct __declspec(align(8)) C_EconWearable {
    char m_pad[5736];
    int32 m_nForceSkin; // Size: 4
};

struct __declspec(align(8)) C_BaseGrenade {
    char m_pad[4384];
    bool m_bHasWarnedAI; // Size: 1
    bool m_bIsSmokeGrenade; // Size: 1
    bool m_bIsLive; // Size: 2
    char m_pad1_4388[1];
    float32 m_DmgRadius; // Size: 4
    char m_flDetonateTime[4];
    float32 m_flWarnAITime; // Size: 4
    float32 m_flDamage; // Size: 8
    char m_pad4_4408[4];
    void* m_iszBounceSound;
    char m_ExplosionSound[12];
    char m_hThrower[24];
    char m_flNextAttack[4];
};

struct __declspec(align(8)) C_PhysicsPropMultiplayer {
};

struct __declspec(align(8)) C_ViewmodelAttachmentModel {
    char m_pad[3984];
    bool m_bShouldFrontFaceCullLeftHanded; // Size: 1
};

struct __declspec(align(8)) C_PredictedViewModel {
    char m_pad[4080];
    Vector m_vPredictedLagOffset; // Size: 12
    QAngle m_targetSpeed; // Size: 12
};

struct __declspec(align(8)) C_CS2WeaponModuleBase {
};

struct __declspec(align(8)) C_StattrakModule {
    char m_pad[3984];
};

struct __declspec(align(8)) C_NametagModule {
    char m_pad[3984];
};

struct __declspec(align(8)) C_KeychainModule {
    char m_pad[3984];
    uint32 m_nKeychainDefID; // Size: 4
};

struct __declspec(align(8)) C_BaseCSGrenadeProjectile {
    char m_pad[4464];
    Vector m_vInitialPosition; // Size: 12
    Vector m_vInitialVelocity; // Size: 12
    int32 m_nBounces; // Size: 8
    char m_pad4_4496[4];
    void* m_nExplodeEffectIndex;
    int32 m_nExplodeEffectTickBegin; // Size: 4
    Vector m_vecExplodeEffectOrigin; // Size: 12
    char m_flSpawnTime[4];
    Vector vecLastTrailLinePos; // Size: 12
    char flNextTrailLineTime[4];
    bool m_bExplodeEffectBegan; // Size: 1
    bool m_bCanCreateGrenadeTrail; // Size: 3
    char m_pad2_4544[2];
    void* m_nSnapshotTrajectoryEffectIndex;
    void* m_hSnapshotTrajectoryParticleSnapshot;
    char m_arrTrajectoryTrailPoints[24];
    char m_arrTrajectoryTrailPointCreationTimes[24];
};

struct __declspec(align(8)) C_SensorGrenadeProjectile {
};

struct __declspec(align(8)) CBreachChargeProjectile {
};

struct __declspec(align(8)) CBumpMineProjectile {
};

struct __declspec(align(8)) CTripWireFireProjectile {
};

struct __declspec(align(8)) C_CSGO_PreviewModel {
    char m_pad[4384];
    void* m_animgraph;
    void* m_animgraphCharacterModeString;
    void* m_defaultAnim;
    char m_nDefaultAnimLoopMode[4];
    float32 m_flInitialModelScale; // Size: 4
};

struct __declspec(align(8)) C_CSGO_PreviewModelAlias_csgo_item_previewmodel {
};

struct __declspec(align(8)) C_WorldModelGloves {
};

struct __declspec(align(8)) C_BulletHitModel {
    char m_pad[3976];
    char m_matLocal[48];
    int32 m_iBoneIndex; // Size: 4
    char m_hPlayerParent[4];
    bool m_bIsHit; // Size: 4
    char m_pad3_4036[3];
    float32 m_flTimeCreated; // Size: 4
};

struct __declspec(align(8)) C_HostageCarriableProp {
};

struct __declspec(align(8)) C_PlantedC4 {
    char m_pad[3984];
    bool m_bBombTicking; // Size: 4
    char m_pad3_3988[3];
    int32 m_nBombSite; // Size: 4
    int32 m_nSourceSoundscapeHash; // Size: 8
    char m_pad4_4000[4];
    EntitySpottedState_t m_entitySpottedState; // Size: 24
    char m_flNextGlow[4];
    char m_flNextBeep[4];
    char m_flC4Blow[4];
    bool m_bCannotBeDefused; // Size: 1
    bool m_bHasExploded; // Size: 3
    char m_pad2_4040[2];
    float32 m_flTimerLength; // Size: 4
    bool m_bBeingDefused; // Size: 4
    char m_pad3_4048[3];
    float32 m_bTriggerWarning; // Size: 4
    float32 m_bExplodeWarning; // Size: 4
    bool m_bC4Activated; // Size: 1
    bool m_bTenSecWarning; // Size: 3
    char m_pad2_4060[2];
    float32 m_flDefuseLength; // Size: 4
    char m_flDefuseCountDown[4];
    bool m_bBombDefused; // Size: 4
    char m_pad3_4072[3];
    char m_hBombDefuser[4];
    char m_hControlPanel[4];
    C_AttributeContainer m_AttributeManager; // Size: 1192
    char m_hDefuserMultimeter[4];
    char m_flNextRadarFlashTime[4];
    bool m_bRadarFlash; // Size: 4
    char m_pad3_5284[3];
    char m_pBombDefuser[4];
    void* m_fLastDefuseTime;
    CBasePlayerController* m_pPredictionOwner; // Size: 8
    Vector m_vecC4ExplodeSpectatePos; // Size: 12
    QAngle m_vecC4ExplodeSpectateAng; // Size: 12
};

struct __declspec(align(8)) C_Multimeter {
    char m_pad[3984];
};

struct __declspec(align(8)) C_Item {
    char m_pad[5736];
};

struct __declspec(align(8)) C_HEGrenadeProjectile {
};

struct __declspec(align(8)) C_FlashbangProjectile {
};

struct __declspec(align(8)) C_Chicken {
    char m_pad[4656];
    char m_hHolidayHatAddon[4];
    bool m_jumpedThisFrame; // Size: 4
    char m_pad3_4664[3];
    void* m_leader;
    C_AttributeContainer m_AttributeManager; // Size: 1192
    bool m_bAttributesInitialized; // Size: 4
    char m_pad3_5868[3];
    char m_hWaterWakeParticles[4];
};

struct __declspec(align(8)) C_RagdollPropAttached {
    char m_pad[4096];
    uint32 m_boneIndexAttached; // Size: 4
    uint32 m_ragdollAttachedObjectIndex; // Size: 4
    Vector m_attachmentPointBoneSpace; // Size: 12
    Vector m_attachmentPointRagdollSpace; // Size: 12
    Vector m_vecOffset; // Size: 12
    float32 m_parentTime; // Size: 4
};

struct __declspec(align(8)) C_BaseCombatCharacter {
    char m_pad[4384];
    char m_hMyWearables[24];
    char m_leftFootAttachment[1];
    char m_rightFootAttachment[3];
    char m_nWaterWakeMode[4];
    float32 m_flWaterWorldZ; // Size: 4
};

struct __declspec(align(8)) C_CSGOViewModel {
    char m_pad[4129];
    bool m_bShouldIgnoreOffsetAndAccuracy; // Size: 3
    char m_pad2_4132[2];
    char m_nLastKnownAssociatedWeaponEntIndex[4];
    bool m_bNeedToQueueHighResComposite; // Size: 80
    char m_pad79_4216[79];
};

struct  C_CSWeaponBase {
    char m_pad[5852];
    float32 m_flFireSequenceStartTime; // Size: 4
    int32 m_nFireSequenceStartTimeChange; // Size: 4
    int32 m_nFireSequenceStartTimeAck; // Size: 4
    char m_ePlayerFireEvent[4];
    char m_ePlayerFireEventAttackType[4];
    char m_seqIdle[4];
    char m_seqFirePrimary[4];
    void* m_seqFireSecondary;
    char m_thirdPersonFireSequences[24];
    char m_hCurrentThirdPersonSequence[4];
    int32 m_nSilencerBoneIndex; // Size: 4
    char m_thirdPersonSequences[56];
    char m_ClientPreviousWeaponState[4];
    char m_iState[4];
    float32 m_flCrosshairDistance; // Size: 4
    int32 m_iAmmoLastCheck; // Size: 4
    int32 m_iAlpha; // Size: 4
    int32 m_iScopeTextureID; // Size: 4
    int32 m_iCrosshairTextureID; // Size: 4
    float32 m_flGunAccuracyPositionDeprecated; // Size: 4
    int32 m_nLastEmptySoundCmdNum; // Size: 4
    uint32 m_nViewModelIndex; // Size: 4
    bool m_bReloadsWithClips; // Size: 4
    char m_pad3_6020[3];
    char m_flTimeWeaponIdle[4];
    bool m_bFireOnEmpty; // Size: 8
    char m_pad7_6032[7];
    char m_OnPlayerPickup[40];
    char m_weaponMode[4];
    float32 m_flTurningInaccuracyDelta; // Size: 4
    Vector m_vecTurningInaccuracyEyeDirLast; // Size: 12
    float32 m_flTurningInaccuracy; // Size: 4
    float32 m_fAccuracyPenalty; // Size: 4
    char m_flLastAccuracyUpdateTime[4];
    float32 m_fAccuracySmoothedForZoom; // Size: 4
    char m_fScopeZoomEndTime[4];
    int32 m_iRecoilIndex; // Size: 4
    float32 m_flRecoilIndex; // Size: 4
    bool m_bBurstMode; // Size: 4
    char m_pad3_6124[3];
    char m_flLastBurstModeChangeTime[4];
    char m_nPostponeFireReadyTicks[4];
    float32 m_flPostponeFireReadyFrac; // Size: 4
    bool m_bInReload; // Size: 1
    bool m_bReloadVisuallyComplete; // Size: 3
    char m_pad2_6140[2];
    char m_flDroppedAtTime[4];
    bool m_bIsHauledBack; // Size: 1
    bool m_bSilencerOn; // Size: 3
    char m_pad2_6148[2];
    char m_flTimeSilencerSwitchComplete[4];
    int32 m_iOriginalTeamNumber; // Size: 4
    int32 m_iMostRecentTeamNumber; // Size: 4
    bool m_bDroppedNearBuyZone; // Size: 4
    char m_pad3_6164[3];
    float32 m_flNextAttackRenderTimeOffset; // Size: 156
    char m_pad152_6320[152];
    bool m_bClearWeaponIdentifyingUGC; // Size: 1
    bool m_bVisualsDataSet; // Size: 1
    bool m_bOldFirstPersonSpectatedState; // Size: 1
    bool m_bUIWeapon; // Size: 1
    int32 m_nCustomEconReloadEventId; // Size: 12
    char m_pad8_6336[8];
    char m_hPrevOwner[4];
    char m_nDropTick[32];
    bool m_donated; // Size: 4
    char m_pad3_6376[3];
    char m_fLastShotTime[4];
    bool m_bWasOwnedByCT; // Size: 1
    bool m_bWasOwnedByTerrorist; // Size: 3
    char m_pad2_6384[2];
    float32 m_gunHeat; // Size: 4
    uint32 m_smokeAttachments; // Size: 4
    char m_lastSmokeTime[4];
    float32 m_flNextClientFireBulletTime; // Size: 4
    float32 m_flNextClientFireBulletTime_Repredict; // Size: 224
    char m_pad220_6624[220];
    C_IronSightController m_IronSightController; // Size: 176
    int32 m_iIronSightMode; // Size: 16
    char m_pad12_6816[12];
    char m_flLastLOSTraceFailureTime[4];
    int32 m_iNumEmptyAttacks; // Size: 92
    char m_pad88_6912[88];
    char m_flLastMagDropRequestTime[4];
};

struct __declspec(align(16)) C_CSWeaponBaseGun {
    char m_pad[6928];
    int32 m_zoomLevel; // Size: 4
    int32 m_iBurstShotsRemaining; // Size: 4
    int32 m_iSilencerBodygroup; // Size: 16
    char m_pad12_6952[12];
    int32 m_silencedModelIndex; // Size: 4
    bool m_inPrecache; // Size: 1
};

struct __declspec(align(16)) C_C4 {
    char m_pad[6928];
    char m_szScreenText[32];
    char m_activeLightParticleIndex[4];
    char m_eActiveLightEffect[4];
    bool m_bStartedArming; // Size: 4
    char m_pad3_6972[3];
    char m_fArmedTime[4];
    bool m_bBombPlacedAnimation; // Size: 1
    bool m_bIsPlantingViaUse; // Size: 7
    char m_pad6_6984[6];
    EntitySpottedState_t m_entitySpottedState; // Size: 24
    int32 m_nSpotRules; // Size: 4
    char m_bPlayedArmingBeeps[7];
};

struct __declspec(align(16)) C_DEagle {
};

struct __declspec(align(16)) C_WeaponElite {
};

struct __declspec(align(16)) C_WeaponNOVA {
};

struct __declspec(align(16)) C_WeaponSawedoff {
};

struct __declspec(align(16)) C_WeaponTaser {
    char m_pad[6960];
    char m_fFireTime[4];
};

struct __declspec(align(16)) C_WeaponXM1014 {
};

struct __declspec(align(16)) C_Knife {
};

struct __declspec(align(16)) C_Melee {
};

struct __declspec(align(16)) C_WeaponShield {
    char m_pad[6960];
};

struct __declspec(align(8)) C_MolotovProjectile {
    char m_pad[4616];
};

struct __declspec(align(8)) C_DecoyProjectile {
    char m_pad[4616];
    int32 m_nDecoyShotTick; // Size: 4
    int32 m_nClientLastKnownDecoyShotTick; // Size: 36
    char m_pad32_4656[32];
};

struct __declspec(align(8)) C_SmokeGrenadeProjectile {
    char m_pad[4624];
    int32 m_nSmokeEffectTickBegin; // Size: 4
    bool m_bDidSmokeEffect; // Size: 4
    char m_pad3_4632[3];
    int32 m_nRandomSeed; // Size: 4
    Vector m_vSmokeColor; // Size: 12
    Vector m_vSmokeDetonationPos; // Size: 16
    char m_VoxelFrameData[24];
    bool m_bSmokeVolumeDataReceived; // Size: 1
};

struct  C_BaseCSGrenade {
    char m_pad[6928];
    bool m_bClientPredictDelete; // Size: 1
    bool m_bRedraw; // Size: 1
    bool m_bIsHeldByPlayer; // Size: 1
    bool m_bPinPulled; // Size: 1
    bool m_bJumpThrow; // Size: 1
    bool m_bThrowAnimating; // Size: 3
    char m_pad2_6936[2];
    char m_fThrowTime[4];
    float32 m_flThrowStrength; // Size: 4
    float32 m_flThrowStrengthApproach; // Size: 4
    char m_fDropTime[4];
    char m_fPinPullTime[4];
    bool m_bJustPulledPin; // Size: 4
    char m_pad3_6960[3];
    char m_nNextHoldTick[4];
    float32 m_flNextHoldFrac; // Size: 4
};

struct  C_WeaponBaseItem {
    char m_pad[6928];
    CountdownTimer m_SequenceCompleteTimer; // Size: 24
};

struct __declspec(align(8)) C_ItemDogtags {
    char m_pad[5992];
    char m_OwningPlayer[4];
};

struct __declspec(align(16)) C_Item_Healthshot {
};

struct __declspec(align(16)) C_Fists {
    char m_pad[6928];
    bool m_bPlayingUninterruptableAct; // Size: 4
    char m_pad3_6932[3];
};

struct __declspec(align(16)) C_SensorGrenade {
};

struct __declspec(align(16)) CBreachCharge {
};

struct __declspec(align(16)) CBumpMine {
};

struct __declspec(align(16)) CTablet {
};

struct __declspec(align(16)) CTripWireFire {
};

struct __declspec(align(16)) CWeaponZoneRepulsor {
};

struct __declspec(align(8)) C_CSPlayerPawnBase {
    char m_pad[4960];
    CCSPlayer_PingServices* m_pPingServices; // Size: 8
    CPlayer_ViewModelServices* m_pViewModelServices; // Size: 8
    char m_fRenderingClipPlane[16];
    int32 m_nLastClipPlaneSetupFrame; // Size: 4
    Vector m_vecLastClipCameraPos; // Size: 12
    Vector m_vecLastClipCameraForward; // Size: 12
    bool m_bClipHitStaticWorld; // Size: 1
    bool m_bCachedPlaneIsValid; // Size: 3
    char m_pad2_5024[2];
    C_CSWeaponBase* m_pClippingWeapon; // Size: 8
    char m_previousPlayerState[4];
    char m_iPlayerState[4];
    bool m_bIsRescuing; // Size: 4
    char m_pad3_5044[3];
    char m_fImmuneToGunGameDamageTime[4];
    char m_fImmuneToGunGameDamageTimeLast[4];
    bool m_bGunGameImmunity; // Size: 1
    bool m_bHasMovedSinceSpawn; // Size: 3
    char m_pad2_5056[2];
    float32 m_fMolotovUseTime; // Size: 4
    float32 m_fMolotovDamageTime; // Size: 4
    int32 m_iThrowGrenadeCounter; // Size: 4
    char m_flLastSpawnTimeIndex[4];
    int32 m_iProgressBarDuration; // Size: 4
    float32 m_flProgressBarStartTime; // Size: 4
    Vector m_vecIntroStartEyePosition; // Size: 12
    Vector m_vecIntroStartPlayerForward; // Size: 12
    char m_flClientDeathTime[4];
    bool m_bScreenTearFrameCaptured; // Size: 4
    char m_pad3_5112[3];
    float32 m_flFlashBangTime; // Size: 4
    float32 m_flFlashScreenshotAlpha; // Size: 4
    float32 m_flFlashOverlayAlpha; // Size: 4
    bool m_bFlashBuildUp; // Size: 1
    bool m_bFlashDspHasBeenCleared; // Size: 1
    bool m_bFlashScreenshotHasBeenGrabbed; // Size: 2
    char m_pad1_5128[1];
    float32 m_flFlashMaxAlpha; // Size: 4
    float32 m_flFlashDuration; // Size: 4
    int32 m_iHealthBarRenderMaskIndex; // Size: 4
    float32 m_flHealthFadeValue; // Size: 4
    float32 m_flHealthFadeAlpha; // Size: 16
    char m_pad12_5160[12];
    float32 m_flDeathCCWeight; // Size: 4
    float32 m_flPrevRoundEndTime; // Size: 4
    float32 m_flPrevMatchEndTime; // Size: 8
    char m_pad4_5176[4];
    QAngle m_angEyeAngles; // Size: 24
    float32 m_fNextThinkPushAway; // Size: 4
    bool m_bShouldAutobuyDMWeapons; // Size: 1
    bool m_bShouldAutobuyNow; // Size: 3
    char m_pad2_5208[2];
    void* m_iIDEntIndex;
    CountdownTimer m_delayTargetIDTimer; // Size: 24
    char m_iTargetItemEntIdx[4];
    char m_iOldIDEntIndex[4];
    CountdownTimer m_holdTargetIDTimer; // Size: 28
    float32 m_flCurrentMusicStartTime; // Size: 4
    float32 m_flMusicRoundStartTime; // Size: 4
    bool m_bDeferStartMusicOnWarmup; // Size: 4
    char m_pad3_5288[3];
    int32 m_cycleLatch; // Size: 4
    float32 m_serverIntendedCycle; // Size: 4
    float32 m_flLastSmokeOverlayAlpha; // Size: 4
    float32 m_flLastSmokeAge; // Size: 4
    Vector m_vLastSmokeOverlayColor; // Size: 12
    char m_nPlayerSmokedFx[4];
    char m_nPlayerInfernoBodyFx[4];
    char m_nPlayerInfernoFootFx[4];
    float32 m_flNextMagDropTime; // Size: 4
    int32 m_nLastMagDropAttachmentIndex; // Size: 4
    Vector m_vecLastAliveLocalVelocity; // Size: 40
    bool m_bGuardianShouldSprayCustomXMark; // Size: 8
    char m_pad7_5384[7];
};

struct __declspec(align(8)) C_Hostage {
    char m_pad[4520];
    EntitySpottedState_t m_entitySpottedState; // Size: 24
    void* m_leader;
    CountdownTimer m_reuseTimer; // Size: 24
    Vector m_vel; // Size: 12
    bool m_isRescued; // Size: 1
    bool m_jumpedThisFrame; // Size: 3
    char m_pad2_4592[2];
    int32 m_nHostageState; // Size: 4
    bool m_bHandsHaveBeenCut; // Size: 4
    char m_pad3_4600[3];
    char m_hHostageGrabber[4];
    char m_fLastGrabTime[4];
    Vector m_vecGrabbedPos; // Size: 12
    char m_flRescueStartTime[4];
    char m_flGrabSuccessTime[4];
    char m_flDropStartTime[4];
    void* m_flDeadOrRescuedTime;
    CountdownTimer m_blinkTimer; // Size: 24
    Vector m_lookAt; // Size: 16
    CountdownTimer m_lookAroundTimer; // Size: 24
    bool m_isInit; // Size: 1
    char m_eyeAttachment[1];
    char m_chestAttachment[6];
    CBasePlayerController* m_pPredictionOwner; // Size: 8
};

struct __declspec(align(8)) C_NetTestBaseCombatCharacter {
};

struct __declspec(align(16)) C_AK47 {
};

struct __declspec(align(16)) C_WeaponAug {
};

struct __declspec(align(16)) C_WeaponAWP {
};

struct __declspec(align(16)) C_WeaponBizon {
};

struct __declspec(align(16)) C_WeaponFamas {
};

struct __declspec(align(16)) C_WeaponFiveSeven {
};

struct __declspec(align(16)) C_WeaponG3SG1 {
};

struct __declspec(align(16)) C_WeaponGalilAR {
};

struct __declspec(align(16)) C_WeaponGlock {
};

struct __declspec(align(16)) C_WeaponHKP2000 {
};

struct __declspec(align(16)) C_WeaponUSPSilencer {
};

struct __declspec(align(16)) C_WeaponM4A1 {
};

struct __declspec(align(16)) C_WeaponM4A1Silencer {
};

struct __declspec(align(16)) C_WeaponMAC10 {
};

struct __declspec(align(16)) C_WeaponMag7 {
};

struct __declspec(align(16)) C_WeaponMP5SD {
};

struct __declspec(align(16)) C_WeaponMP7 {
};

struct __declspec(align(16)) C_WeaponMP9 {
};

struct __declspec(align(16)) C_WeaponNegev {
};

struct __declspec(align(16)) C_WeaponP250 {
};

struct __declspec(align(16)) C_WeaponCZ75a {
};

struct __declspec(align(16)) C_WeaponP90 {
};

struct __declspec(align(16)) C_WeaponSCAR20 {
};

struct __declspec(align(16)) C_WeaponSG556 {
};

struct __declspec(align(16)) C_WeaponSSG08 {
};

struct __declspec(align(16)) C_WeaponTec9 {
};

struct __declspec(align(16)) C_WeaponUMP45 {
};

struct __declspec(align(16)) C_WeaponM249 {
};

struct __declspec(align(16)) C_WeaponRevolver {
};

struct __declspec(align(16)) C_MolotovGrenade {
};

struct __declspec(align(16)) C_IncendiaryGrenade {
};

struct __declspec(align(16)) C_DecoyGrenade {
};

struct __declspec(align(16)) C_Flashbang {
};

struct __declspec(align(16)) C_HEGrenade {
};

struct __declspec(align(16)) C_SmokeGrenade {
};

struct __declspec(align(16)) C_CSGO_PreviewPlayer {
    char m_pad[14896];
    void* m_animgraph;
    void* m_animgraphCharacterModeString;
};

struct __declspec(align(16)) C_CSGO_PreviewPlayerAlias_csgo_player_previewmodel {
};```
