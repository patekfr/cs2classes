# cs2classes
my discord: patekfr

client.dll

```
struct  CScriptComponent {
    char m_pad[48];
    CUtlSymbolLarge m_scriptClassName; 
};

struct __declspec(align(8))  C_BaseEntity {
    char m_pad[56];
    CBodyComponent* m_CBodyComponent; // Size: 8
    CNetworkTransmitComponent m_NetworkTransmitComponent; // Size: 736
    GameTick_t m_nLastThinkTick; // Size: 8
    CGameSceneNode* m_pGameSceneNode; // Size: 8
    CRenderComponent* m_pRenderComponent; // Size: 8
    CCollisionProperty* m_pCollision; // Size: 8
    int32 m_iMaxHealth; 
    int32 m_iHealth; 
    uint8 m_lifeState; 
    char m_pad6_848[6];
    bool m_bTakesDamage; 
    TakeDamageFlags_t m_nTakeDamageFlags; // Size: 8
    EntityPlatformTypes_t m_nPlatformType; 
    char m_pad2_860[2];
    uint8 m_ubInterpolationFrame; 
    CHandle< C_BaseEntity > m_hSceneObjectController; 
    int32 m_nNoInterpolationTick; 
    int32 m_nVisibilityNoInterpolationTick; 
    float32 m_flProxyRandomValue; 
    int32 m_iEFlags; 
    uint8 m_nWaterType; 
    bool m_bInterpolateEvenWithNoModel; 
    bool m_bPredictionEligible; 
    bool m_bApplyLayerMatchIDToModel; 
    CUtlStringToken m_tokLayerMatchID; 
    CUtlStringToken m_nSubclassID; // Size: 16
    int32 m_nSimulationTick; 
    int32 m_iCurrentThinkContext; 
    CUtlVector< thinkfunc_t > m_aThinkFunctions; // Size: 24
    char m_pad3_940[3];
    bool m_bDisabledContextThinks; 
    float32 m_flAnimTime; 
    float32 m_flSimulationTime; 
    uint8 m_nSceneObjectOverrideFlags; 
    bool m_bHasSuccessfullyInterpolated; 
    bool m_bHasAddedVarsToInterpolation; 
    bool m_bRenderEvenWhenNotSuccessfullyInterpolated; 
    int32[2] m_nInterpolationLatchDirtyFlags; // Size: 8
    uint16[11] m_ListEntry; // Size: 24
    GameTime_t m_flCreateTime; 
    float32 m_flSpeed; 
    uint16 m_EntClientFlags; 
    bool m_bClientSideRagdoll; 
    uint8 m_iTeamNum; 
    uint32 m_spawnflags; 
    GameTick_t m_nNextThinkTick; 
    uint32 m_fFlags; 
    Vector m_vecAbsVelocity; // Size: 16
    CNetworkVelocityVector m_vecVelocity; // Size: 48
    Vector m_vecBaseVelocity; // Size: 12
    CHandle< C_BaseEntity > m_hEffectEntity; 
    CHandle< C_BaseEntity > m_hOwnerEntity; 
    MoveCollide_t m_MoveCollide; 
    MoveType_t m_MoveType; 
    MoveType_t m_nActualMoveType; 
    float32 m_flWaterLevel; 
    uint32 m_fEffects; 
    CHandle< C_BaseEntity > m_hGroundEntity; 
    int32 m_nGroundBodyIndex; 
    float32 m_flFriction; 
    float32 m_flElasticity; 
    float32 m_flGravityScale; 
    float32 m_flTimeScale; 
    char m_pad3_1132[3];
    bool m_bAnimatedEveryTick; 
    GameTime_t m_flNavIgnoreUntilTime; 
    char m_pad14_1152[14];
    uint16 m_hThink; // Size: 16
    uint8 m_fBBoxVisFlags; 
    bool m_bPredictable; 
    char m_pad1_1156[1];
    bool m_bRenderWithViewModels; 
    CSplitScreenSlot m_nSplitUserPlayerPredictionSlot; 
    int32 m_nFirstPredictableCommand; 
    int32 m_nLastPredictableCommand; 
    CHandle< C_BaseEntity > m_hOldMoveParent; // Size: 8
    CParticleProperty m_Particles; // Size: 40
    CUtlVector< float32 > m_vecPredictedScriptFloats; // Size: 24
    CUtlVector< int32 > m_vecPredictedScriptFloatIDs; // Size: 48
    char m_pad12_1304[12];
    int32 m_nNextScriptVarRecordID; // Size: 16
    QAngle m_vecAngVelocity; // Size: 12
    int32 m_DataChangeEventRef; 
    CUtlVector< CEntityHandle > m_dependencies; // Size: 24
    char m_pad9_1357[9];
    int32 m_nCreationTick; // Size: 13
    bool m_bAnimTimeChanged; 
    char m_pad9_1368[9];
    bool m_bSimulationTimeChanged; // Size: 10
    CUtlString m_sUniqueHammerID; // Size: 8
    BloodType m_nBloodType; 
};

struct  CountdownTimer {
    char m_pad[8];
    float32 m_duration; 
    GameTime_t m_timestamp; 
    float32 m_timescale; 
    WorldGroupId_t m_nWorldGroupId; 
};

struct  CEntityComponent {
};

struct  CEntityIdentity {
    char m_pad[20];
    int32 m_nameStringableIndex; 
    CUtlSymbolLarge m_name; // Size: 8
    CUtlSymbolLarge m_designerName; // Size: 16
    char m_pad4_56[4];
    uint32 m_flags; // Size: 8
    WorldGroupId_t m_worldGroupId; 
    uint32 m_fDataObjectTypes; 
    ChangeAccessorFieldPathIndex_t m_PathIndex; // Size: 24
    CEntityIdentity* m_pPrev; // Size: 8
    CEntityIdentity* m_pNext; // Size: 8
    CEntityIdentity* m_pPrevByClass; // Size: 8
    CEntityIdentity* m_pNextByClass; 
};

struct  CEntityInstance {
    char m_pad[8];
    CUtlSymbolLarge m_iszPrivateVScripts; // Size: 8
    CEntityIdentity* m_pEntity; // Size: 24
    CScriptComponent* m_CScriptComponent; // Size: 8
    bool m_bVisibleinPVS; 
};

struct  CGameSceneNode {
    char m_pad[16];
    CTransform m_nodeToWorld; // Size: 32
    CEntityInstance* m_pOwner; // Size: 8
    CGameSceneNode* m_pParent; // Size: 8
    CGameSceneNode* m_pChild; // Size: 8
    CGameSceneNode* m_pNextSibling; // Size: 48
    CGameSceneNodeHandle m_hParent; // Size: 16
    CNetworkOriginCellCoordQuantizedVector m_vecOrigin; // Size: 56
    QAngle m_angRotation; // Size: 12
    float32 m_flScale; 
    Vector m_vecAbsOrigin; // Size: 12
    QAngle m_angAbsRotation; // Size: 12
    float32 m_flAbsScale; 
    int16 m_nParentAttachmentOrBone; 
    bool m_bDebugAbsOriginChanges; 
    bool m_bDormant; 
    bool m_bForceParentToBeNetworked; 
    bitfield:1 m_bDirtyHierarchy; 
    bitfield:1 m_bDirtyBoneMergeInfo; 
    bitfield:1 m_bNetworkedPositionChanged; 
    bitfield:1 m_bNetworkedAnglesChanged; 
    bitfield:1 m_bNetworkedScaleChanged; 
    bitfield:1 m_bWillBeCallingPostDataUpdate; 
    bitfield:1 m_bBoneMergeFlex; 
    bitfield:2 m_nLatchAbsOrigin; 
    bitfield:1 m_bDirtyBoneMergeBoneToRoot; // Size: 243
    uint8 m_nHierarchicalDepth; 
    uint8 m_nHierarchyType; 
    char m_pad2_248[2];
    uint8 m_nDoNotSetAnimTimeInInvalidatePhysicsCount; 
    CUtlStringToken m_name; // Size: 64
    CUtlStringToken m_hierarchyAttachName; 
    float32 m_flZOffset; 
    float32 m_flClientLocalScale; 
    Vector m_vRenderOrigin; 
};

struct  CBodyComponent {
    char m_pad[8];
    CGameSceneNode* m_pSceneNode; // Size: 24
    CNetworkVarChainer __m_pChainEntity; 
};

struct  CBodyComponentPoint {
    char m_pad[80];
    CGameSceneNode m_sceneNode; 
};

struct  CSkeletonInstance {
    char m_pad[368];
    CModelState m_modelState; // Size: 560
    bool m_bIsAnimationEnabled; 
    bool m_bUseParentRenderBounds; 
    bool m_bDisableSolidCollisionsForHierarchy; 
    bitfield:1 m_bDirtyMotionType; 
    bitfield:1 m_bIsGeneratingLatchedParentSpaceState; // Size: 932
    CUtlStringToken m_materialGroup; 
    uint8 m_nHitboxSet; 
};

struct  CBodyComponentSkeletonInstance {
    char m_pad[80];
    CSkeletonInstance m_skeletonInstance; 
};

struct  CHitboxComponent {
    char m_pad[36];
    uint32[1] m_bvDisabledHitGroups; 
};

struct  CLightComponent {
    char m_pad[56];
    CNetworkVarChainer __m_pChainEntity; // Size: 61
    Color m_Color; 
    Color m_SecondaryColor; 
    float32 m_flBrightness; 
    float32 m_flBrightnessScale; 
    float32 m_flBrightnessMult; 
    float32 m_flRange; 
    float32 m_flFalloff; 
    float32 m_flAttenuation0; 
    float32 m_flAttenuation1; 
    float32 m_flAttenuation2; 
    float32 m_flTheta; 
    float32 m_flPhi; 
    CStrongHandle< InfoForResourceTypeCTextureBase > m_hLightCookie; // Size: 8
    int32 m_nCascades; 
    int32 m_nCastShadows; 
    int32 m_nShadowWidth; 
    int32 m_nShadowHeight; 
    char m_pad3_196[3];
    bool m_bRenderDiffuse; 
    int32 m_nRenderSpecular; 
    char m_pad3_204[3];
    bool m_bRenderTransmissive; 
    float32 m_flOrthoLightWidth; 
    float32 m_flOrthoLightHeight; 
    int32 m_nStyle; 
    CUtlString m_Pattern; // Size: 8
    int32 m_nCascadeRenderStaticObjects; 
    float32 m_flShadowCascadeCrossFade; 
    float32 m_flShadowCascadeDistanceFade; 
    float32 m_flShadowCascadeDistance0; 
    float32 m_flShadowCascadeDistance1; 
    float32 m_flShadowCascadeDistance2; 
    float32 m_flShadowCascadeDistance3; 
    int32 m_nShadowCascadeResolution0; 
    int32 m_nShadowCascadeResolution1; 
    int32 m_nShadowCascadeResolution2; 
    int32 m_nShadowCascadeResolution3; 
    char m_pad3_272[3];
    bool m_bUsesBakedShadowing; 
    int32 m_nShadowPriority; 
    int32 m_nBakedShadowIndex; 
    char m_pad3_284[3];
    bool m_bRenderToCubemaps; 
    int32 m_nDirectLight; 
    int32 m_nIndirectLight; 
    float32 m_flFadeMinDist; 
    float32 m_flFadeMaxDist; 
    float32 m_flShadowFadeMinDist; 
    float32 m_flShadowFadeMaxDist; 
    bool m_bEnabled; 
    bool m_bFlicker; 
    char m_pad1_312[1];
    bool m_bPrecomputedFieldsValid; 
    Vector m_vPrecomputedBoundsMins; // Size: 12
    Vector m_vPrecomputedBoundsMaxs; // Size: 12
    Vector m_vPrecomputedOBBOrigin; // Size: 12
    QAngle m_vPrecomputedOBBAngles; // Size: 12
    Vector m_vPrecomputedOBBExtent; // Size: 12
    float32 m_flPrecomputedMaxRange; 
    int32 m_nFogLightingMode; 
    float32 m_flFogContributionStength; 
    float32 m_flNearClipPlane; 
    Color m_SkyColor; 
    float32 m_flSkyIntensity; 
    Color m_SkyAmbientBounce; 
    bool m_bUseSecondaryColor; 
    char m_pad2_404[2];
    bool m_bMixedShadows; 
    GameTime_t m_flLightStyleStartTime; 
    float32 m_flCapsuleLength; 
    float32 m_flMinRoughness; 
};

struct  CRenderComponent {
    char m_pad[16];
    CNetworkVarChainer __m_pChainEntity; // Size: 64
    char m_pad3_84[3];
    bool m_bIsRenderingWithViewModels; 
    char m_pad8_96[8];
    uint32 m_nSplitscreenFlags; // Size: 12
    char m_pad79_176[79];
    bool m_bEnableRendering; // Size: 80
    bool m_bInterpolationReadyToDraw; 
};

struct __declspec(align(8))  C_PointCamera {
    char m_pad[1384];
    float32 m_FOV; 
    float32 m_Resolution; 
    bool m_bFogEnable; 
    Color m_FogColor; 
    float32 m_flFogStart; 
    float32 m_flFogEnd; 
    float32 m_flFogMaxDensity; 
    bool m_bActive; 
    char m_pad2_1416[2];
    bool m_bUseScreenAspectRatio; 
    float32 m_flAspectRatio; 
    char m_pad3_1424[3];
    bool m_bNoSky; 
    float32 m_fBrightness; 
    float32 m_flZFar; 
    float32 m_flZNear; 
    bool m_bCanHLTVUse; 
    bool m_bAlignWithParent; 
    char m_pad1_1440[1];
    bool m_bDofEnabled; 
    float32 m_flDofNearBlurry; 
    float32 m_flDofNearCrisp; 
    float32 m_flDofFarCrisp; 
    float32 m_flDofFarBlurry; 
    float32 m_flDofTiltToGround; 
    float32 m_TargetFOV; 
    float32 m_DegreesPerSecond; 
    char m_pad3_1472[3];
    bool m_bIsOn; 
    C_PointCamera* m_pNext; 
};

struct  CPointTemplateAPI {
};

struct  CPropDataComponent {
    char m_pad[16];
    float32 m_flDmgModBullet; 
    float32 m_flDmgModClub; 
    float32 m_flDmgModExplosive; 
    float32 m_flDmgModFire; 
    CUtlSymbolLarge m_iszPhysicsDamageTableName; // Size: 8
    CUtlSymbolLarge m_iszBasePropData; // Size: 8
    int32 m_nInteractions; 
    char m_pad3_56[3];
    bool m_bSpawnMotionDisabled; 
    int32 m_nDisableTakePhysicsDamageSpawnFlag; 
    int32 m_nMotionDisabledSpawnFlag; 
};

struct  CBuoyancyHelper {
    char m_pad[24];
    CUtlStringToken m_nFluidType; 
    float32 m_flFluidDensity; 
    CUtlVector< float32 > m_vecFractionOfWheelSubmergedForWheelFriction; // Size: 24
    CUtlVector< float32 > m_vecWheelFrictionScales; // Size: 24
    CUtlVector< float32 > m_vecFractionOfWheelSubmergedForWheelDrag; // Size: 24
    CUtlVector< float32 > m_vecWheelDrag; 
};

struct __declspec(align(8))  CBaseAnimGraph {
    char m_pad[3488];
    char m_pad1_3490[1];
    bool m_bInitiallyPopulateInterpHistory; 
    char m_pad13_3504[13];
    bool m_bSuppressAnimEventSounds; // Size: 14
    char m_pad3_3508[3];
    bool m_bAnimGraphUpdateEnabled; 
    float32 m_flMaxSlopeDistance; 
    Vector m_vLastSlopeCheckPos; // Size: 12
    char m_pad3_3528[3];
    bool m_bAnimationUpdateScheduled; 
    Vector m_vecForce; // Size: 12
    int32 m_nForceBone; 
    CBaseAnimGraph* m_pClientsideRagdoll; // Size: 8
    char m_pad23_3576[23];
    bool m_bBuiltRagdoll; // Size: 24
    PhysicsRagdollPose_t m_RagdollPose; // Size: 72
    char m_pad15_3664[15];
    bool m_bRagdollClientSide; // Size: 16
    bool m_bHasAnimatedMaterialAttributes; 
};

struct  CSharedGapTypeQueryRegistration {
};

struct  CBasePlayerControllerAPI {
};

struct  C_CommandContext {
    char m_pad159_160[159];
    bool needsprocessing; // Size: 160
    char m_pad[160];
    int32 command_number; 
};

struct  ViewAngleServerChange_t {
    char m_pad[48];
    FixAngleSet_t nType; 
    QAngle qAngle; // Size: 12
    uint32 nIndex; 
};

struct  CPlayer_AutoaimServices {
};

struct  audioparams_t {
    char m_pad[8];
    Vector[8] localSound; // Size: 96
    int32 soundscapeIndex; 
    char m_pad3_112[3];
    uint8 localBits; 
    int32 soundscapeEntityListIndex; 
    uint32 soundEventHash; 
};

struct  C_fogplayerparams_t {
    char m_pad[8];
    CHandle< C_FogController > m_hCtrl; 
    float32 m_flTransitionTime; 
    Color m_OldColor; 
    float32 m_flOldStart; 
    float32 m_flOldEnd; 
    float32 m_flOldMaxDensity; 
    float32 m_flOldHDRColorScale; 
    float32 m_flOldFarZ; 
    Color m_NewColor; 
    float32 m_flNewStart; 
    float32 m_flNewEnd; 
    float32 m_flNewMaxDensity; 
    float32 m_flNewHDRColorScale; 
    float32 m_flNewFarZ; 
};

struct __declspec(align(8))  C_ColorCorrection {
    char m_pad[1384];
    Vector m_vecOrigin; // Size: 12
    float32 m_MinFalloff; 
    float32 m_MaxFalloff; 
    float32 m_flFadeInDuration; 
    float32 m_flFadeOutDuration; 
    float32 m_flMaxWeight; 
    float32 m_flCurWeight; 
    char[512] m_netlookupFilename; // Size: 512
    bool m_bEnabled; 
    bool m_bMaster; 
    bool m_bClientSide; 
    bool m_bExclusive; 
    bool[1] m_bEnabledOnClient; 
    float32[1] m_flCurWeightOnClient; 
    bool[1] m_bFadingIn; 
    float32[1] m_flFadeStartWeight; 
    float32[1] m_flFadeStartTime; 
    float32[1] m_flFadeDuration; 
};

struct __declspec(align(8))  C_TonemapController2 {
    char m_pad[1384];
    float32 m_flAutoExposureMin; 
    float32 m_flAutoExposureMax; 
    float32 m_flTonemapPercentTarget; 
    float32 m_flTonemapPercentBrightPixels; 
    float32 m_flTonemapMinAvgLum; 
    float32 m_flExposureAdaptationSpeedUp; 
    float32 m_flExposureAdaptationSpeedDown; 
    float32 m_flTonemapEVSmoothingRange; 
};

struct __declspec(align(8))  C_PostProcessingVolume {
    char m_pad[3392];
    CStrongHandle< InfoForResourceTypeCPostProcessingResource > m_hPostSettings; // Size: 8
    float32 m_flFadeDuration; 
    float32 m_flMinLogExposure; 
    float32 m_flMaxLogExposure; 
    float32 m_flMinExposure; 
    float32 m_flMaxExposure; 
    float32 m_flExposureCompensation; 
    float32 m_flExposureFadeSpeedUp; 
    float32 m_flExposureFadeSpeedDown; 
    float32 m_flTonemapEVSmoothingRange; 
    bool m_bMaster; 
    char m_pad2_3440[2];
    bool m_bExposureControl; 
    float32 m_flRate; 
    float32 m_flTonemapPercentTarget; 
    float32 m_flTonemapPercentBrightPixels; 
    float32 m_flTonemapMinAvgLum; 
};

struct  fogparams_t {
    char m_pad[8];
    Vector dirPrimary; // Size: 12
    Color colorPrimary; 
    Color colorSecondary; 
    Color colorPrimaryLerpTo; 
    Color colorSecondaryLerpTo; 
    float32 start; 
    float32 end; 
    float32 farz; 
    float32 maxdensity; 
    float32 exponent; 
    float32 HDRColorScale; 
    float32 skyboxFogFactor; 
    float32 skyboxFogFactorLerpTo; 
    float32 startLerpTo; 
    float32 endLerpTo; 
    float32 maxdensityLerpTo; 
    GameTime_t lerptime; 
    float32 duration; 
    float32 blendtobackground; 
    float32 scattering; 
    float32 locallightscale; 
    bool enable; 
    bool blend; 
    bool m_bNoReflectionFog; 
    bool m_bPadding; 
};

struct __declspec(align(8))  C_FogController {
    char m_pad[1384];
    fogparams_t m_fog; // Size: 104
    char m_pad3_1492[3];
    bool m_bUseAngles; 
    int32 m_iChangedVariables; 
};

struct  CPlayer_CameraServices {
    char m_pad[64];
    QAngle m_vecCsViewPunchAngle; // Size: 12
    GameTick_t m_nCsViewPunchAngleTick; 
    char m_pad4_88[4];
    float32 m_flCsViewPunchAngleTickRatio; // Size: 8
    C_fogplayerparams_t m_PlayerFog; // Size: 64
    CHandle< C_ColorCorrection > m_hColorCorrectionCtrl; 
    CHandle< C_BaseEntity > m_hViewEntity; 
    CHandle< C_TonemapController2 > m_hTonemapController; // Size: 8
    audioparams_t m_audio; // Size: 120
    C_NetworkUtlVectorBase< CHandle< C_PostProcessingVolume > > m_PostProcessingVolumes; // Size: 24
    float32 m_flOldPlayerZ; 
    float32 m_flOldPlayerViewOffsetZ; 
    fogparams_t m_CurrentFog; // Size: 104
    CHandle< C_FogController > m_hOldFogController; 
    bool[5] m_bOverrideFogColor; 
    Color[5] m_OverrideFogColor; // Size: 20
    bool[5] m_bOverrideFogStartEnd; 
    float32[5] m_fOverrideFogStart; // Size: 20
    float32[5] m_fOverrideFogEnd; // Size: 20
    CHandle< C_PostProcessingVolume > m_hActivePostProcessingVolume; 
    QAngle m_angDemoViewAngles; 
};

struct  CPlayer_FlashlightServices {
};

struct  CPlayer_ItemServices {
};

struct  CPlayer_MovementServices {
    char m_pad[64];
    char m_pad4_72[4];
    int32 m_nImpulse; // Size: 8
    CInButtonState m_nButtons; // Size: 32
    uint64 m_nQueuedButtonDownMask; // Size: 8
    uint64 m_nQueuedButtonChangeMask; // Size: 8
    uint64 m_nButtonDoublePressed; // Size: 8
    uint32[64] m_pButtonPressedCmdNumber; // Size: 256
    char m_pad4_392[4];
    uint32 m_nLastCommandNumberProcessed; // Size: 8
    char m_pad8_408[8];
    uint64 m_nToggleButtonDownMask; // Size: 16
    float32 m_flMaxspeed; 
    float32[4] m_arrForceSubtickMoveWhen; // Size: 16
    float32 m_flForwardMove; 
    float32 m_flLeftMove; 
    float32 m_flUpMove; 
    Vector m_vecLastMovementImpulses; // Size: 12
    QAngle m_vecOldViewAngles; 
};

struct  CPlayer_MovementServices_Humanoid {
    char m_pad[472];
    float32 m_flStepSoundTime; 
    float32 m_flFallVelocity; 
    char m_pad3_484[3];
    bool m_bInCrouch; 
    uint32 m_nCrouchState; 
    GameTime_t m_flCrouchTransitionStartTime; 
    bool m_bDucked; 
    bool m_bDucking; 
    char m_pad1_496[1];
    bool m_bInDuckJump; 
    Vector m_groundNormal; // Size: 12
    float32 m_flSurfaceFriction; 
    CUtlStringToken m_surfaceProps; // Size: 16
    int32 m_nStepside; 
};

struct  CPlayer_ObserverServices {
    char m_pad[64];
    char m_pad3_68[3];
    uint8 m_iObserverMode; 
    CHandle< C_BaseEntity > m_hObserverTarget; 
    ObserverMode_t m_iObserverLastMode; 
    char m_pad3_80[3];
    bool m_bForcedObserverMode; 
    float32 m_flObserverChaseDistance; 
    GameTime_t m_flObserverChaseDistanceCalcTime; 
};

struct  CPlayer_UseServices {
};

struct  CPlayer_WaterServices {
};

struct __declspec(align(8))  C_BasePlayerWeapon {
    char m_pad[5736];
    GameTick_t m_nNextPrimaryAttackTick; 
    float32 m_flNextPrimaryAttackTickRatio; 
    GameTick_t m_nNextSecondaryAttackTick; 
    float32 m_flNextSecondaryAttackTickRatio; 
    int32 m_iClip1; 
    int32 m_iClip2; 
    int32[2] m_pReserveAmmo; 
};

struct  CPlayer_WeaponServices {
    char m_pad[64];
    C_NetworkUtlVectorBase< CHandle< C_BasePlayerWeapon > > m_hMyWeapons; // Size: 24
    CHandle< C_BasePlayerWeapon > m_hActiveWeapon; 
    CHandle< C_BasePlayerWeapon > m_hLastWeapon; 
    uint16[32] m_iAmmo; 
};

struct  CBaseAnimGraphController {
    char m_pad[24];
    CAnimGraphNetworkedVariables m_animGraphNetworkedVars; // Size: 5264
    char m_pad3_5292[3];
    bool m_bSequenceFinished; 
    float32 m_flSoundSyncTime; 
    uint32 m_nActiveIKChainMask; 
    HSequence m_hSequence; 
    GameTime_t m_flSeqStartTime; 
    float32 m_flSeqFixedCycle; 
    AnimLoopMode_t m_nAnimLoopMode; 
    CNetworkedQuantizedFloat m_flPlaybackRate; // Size: 12
    SequenceFinishNotifyState_t m_nNotifyState; 
    bool m_bNetworkedAnimationInputsChanged; 
    bool m_bNetworkedSequenceChanged; 
    char m_pad3_5336[3];
    bool m_bLastUpdateSkipped; 
    GameTime_t m_flPrevAnimUpdateTime; 
};

struct  CBodyComponentBaseAnimGraph {
    char m_pad[1168];
    CBaseAnimGraphController m_animationController; 
};

struct  EntityRenderAttribute_t {
    char m_pad[48];
    CUtlStringToken m_ID; 
    Vector4D m_Values; 
};

struct __declspec(align(8))  C_BaseModelEntity {
    char m_pad[2640];
    CRenderComponent* m_CRenderComponent; // Size: 8
    CHitboxComponent m_CHitboxComponent; // Size: 40
    HitGroup_t m_LastHitGroup; // Size: 40
    bool m_bInitModelEffects; 
    char m_pad2_2732[2];
    bool m_bIsStaticProp; 
    int32 m_nLastAddDecal; 
    int32 m_nDecalsAdded; 
    int32 m_iOldHealth; 
    RenderMode_t m_nRenderMode; 
    RenderFx_t m_nRenderFX; 
    char m_pad29_2776[29];
    bool m_bAllowFadeInView; // Size: 30
    Color m_clrRender; // Size: 8
    C_UtlVectorEmbeddedNetworkVar< EntityRenderAttribute_t > m_vecRenderAttributes; // Size: 104
    bool m_bRenderToCubemaps; 
    char m_pad6_2896[6];
    bool m_bNoInterpolate; 
    CCollisionProperty m_Collision; // Size: 176
    CGlowProperty m_Glow; // Size: 88
    float32 m_flGlowBackfaceMult; 
    float32 m_fadeMinDist; 
    float32 m_fadeMaxDist; 
    float32 m_flFadeScale; 
    float32 m_flShadowStrength; 
    char m_pad3_3184[3];
    uint8 m_nObjectCulling; 
    int32 m_nAddDecal; 
    Vector m_vDecalPosition; // Size: 12
    Vector m_vDecalForwardAxis; // Size: 12
    float32 m_flDecalHealBloodRate; 
    char m_pad4_3224[4];
    float32 m_flDecalHealHeightRate; // Size: 8
    C_NetworkUtlVectorBase< CHandle< C_BaseModelEntity > > m_ConfigEntitiesToPropagateMaterialDecalsTo; // Size: 24
    CNetworkViewOffsetVector m_vecViewOffset; // Size: 48
    CClientAlphaProperty* m_pClientAlphaProperty; // Size: 8
    Color m_ClientOverrideTint; 
    bool m_bUseClientOverrideTint; 
};

struct  ActiveModelConfig_t {
    char m_pad[40];
    ModelConfigHandle_t m_Handle; // Size: 8
    CUtlSymbolLarge m_Name; // Size: 8
    C_NetworkUtlVectorBase< CHandle< C_BaseModelEntity > > m_AssociatedEntities; // Size: 24
    C_NetworkUtlVectorBase< CUtlSymbolLarge > m_AssociatedEntityNames; 
};

struct  CBodyComponentBaseModelEntity {
};

struct  CGameSceneNodeHandle {
    char m_pad[8];
    CEntityHandle m_hOwner; 
    CUtlStringToken m_name; 
};

struct  CPathSimpleAPI {
};

struct  SequenceHistory_t {
    HSequence m_hSequence; 
    char m_pad[4];
    GameTime_t m_flSeqStartTime; 
    float32 m_flSeqFixedCycle; 
    AnimLoopMode_t m_nSeqLoopMode; 
    float32 m_flPlaybackRate; 
    float32 m_flCyclesPerSecond; 
};

struct  CNetworkedSequenceOperation {
    char m_pad[8];
    HSequence m_hSequence; 
    float32 m_flPrevCycle; 
    float32 m_flCycle; 
    CNetworkedQuantizedFloat m_flWeight; // Size: 8
    bool m_bSequenceChangeNetworked; 
    char m_pad2_32[2];
    bool m_bDiscontinuity; 
    float32 m_flPrevCycleFromDiscontinuity; 
    float32 m_flPrevCycleForAnimEventDetection; 
};

struct  CModelState {
    char m_pad[160];
    CStrongHandle< InfoForResourceTypeCModel > m_hModel; // Size: 8
    CUtlSymbolLarge m_ModelName; // Size: 64
    char m_pad175_408[175];
    bool m_bClientClothCreationSuppressed; // Size: 176
    char m_pad122_538[122];
    uint64 m_MeshGroupMask; // Size: 130
    int8 m_nIdealMotionType; 
    int8 m_nForceLOD; 
    int8 m_nClothUpdateFlags; 
};

struct  IntervalTimer {
    char m_pad[8];
    GameTime_t m_timestamp; 
    WorldGroupId_t m_nWorldGroupId; 
};

struct  EngineCountdownTimer {
    char m_pad[8];
    float32 m_duration; 
    float32 m_timestamp; 
    float32 m_timescale; 
};

struct  CTimeline {
    char m_pad[16];
    float32[64] m_flValues; // Size: 256
    int32[64] m_nValueCounts; // Size: 256
    int32 m_nBucketCount; 
    float32 m_flInterval; 
    float32 m_flFinalValue; 
    TimelineCompression_t m_nCompressionType; 
    bool m_bStopped; 
};

struct  CAnimGraphNetworkedVariables {
    char m_pad[8];
    C_NetworkUtlVectorBase< uint32 > m_PredNetBoolVariables; // Size: 24
    C_NetworkUtlVectorBase< uint8 > m_PredNetByteVariables; // Size: 24
    C_NetworkUtlVectorBase< uint16 > m_PredNetUInt16Variables; // Size: 24
    C_NetworkUtlVectorBase< int32 > m_PredNetIntVariables; // Size: 24
    C_NetworkUtlVectorBase< uint32 > m_PredNetUInt32Variables; // Size: 24
    C_NetworkUtlVectorBase< uint64 > m_PredNetUInt64Variables; // Size: 24
    C_NetworkUtlVectorBase< float32 > m_PredNetFloatVariables; // Size: 24
    C_NetworkUtlVectorBase< Vector > m_PredNetVectorVariables; // Size: 24
    C_NetworkUtlVectorBase< Quaternion > m_PredNetQuaternionVariables; // Size: 24
    C_NetworkUtlVectorBase< CGlobalSymbol > m_PredNetGlobalSymbolVariables; // Size: 24
    C_NetworkUtlVectorBase< uint32 > m_OwnerOnlyPredNetBoolVariables; // Size: 24
    C_NetworkUtlVectorBase< uint8 > m_OwnerOnlyPredNetByteVariables; // Size: 24
    C_NetworkUtlVectorBase< uint16 > m_OwnerOnlyPredNetUInt16Variables; // Size: 24
    C_NetworkUtlVectorBase< int32 > m_OwnerOnlyPredNetIntVariables; // Size: 24
    C_NetworkUtlVectorBase< uint32 > m_OwnerOnlyPredNetUInt32Variables; // Size: 24
    C_NetworkUtlVectorBase< uint64 > m_OwnerOnlyPredNetUInt64Variables; // Size: 24
    C_NetworkUtlVectorBase< float32 > m_OwnerOnlyPredNetFloatVariables; // Size: 24
    C_NetworkUtlVectorBase< Vector > m_OwnerOnlyPredNetVectorVariables; // Size: 24
    C_NetworkUtlVectorBase< Quaternion > m_OwnerOnlyPredNetQuaternionVariables; // Size: 24
    C_NetworkUtlVectorBase< CGlobalSymbol > m_OwnerOnlyPredNetGlobalSymbolVariables; // Size: 24
    int32 m_nBoolVariablesCount; 
    int32 m_nOwnerOnlyBoolVariablesCount; 
    int32 m_nRandomSeedOffset; 
    float32 m_flLastTeleportTime; 
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
    uint8 m_usSolidFlags; 
    SolidType_t m_nSolidType; 
    uint8 m_triggerBloat; 
    SurroundingBoundsType_t m_nSurroundType; 
    uint8 m_CollisionGroup; 
    uint8 m_nEnablePhysics; 
    float32 m_flBoundingRadius; 
    Vector m_vecSpecifiedSurroundingMins; // Size: 12
    Vector m_vecSpecifiedSurroundingMaxs; // Size: 12
    Vector m_vecSurroundingMaxs; // Size: 12
    Vector m_vecSurroundingMins; // Size: 12
    Vector m_vCapsuleCenter1; // Size: 12
    Vector m_vCapsuleCenter2; // Size: 12
    float32 m_flCapsuleRadius; 
};

struct __declspec(align(8))  CBasePlayerController {
    char m_pad[1392];
    char m_pad4_1400[4];
    int32 m_nFinalPredictedTick; // Size: 8
    C_CommandContext m_CommandContext; // Size: 168
    uint64 m_nInButtonsWhichAreToggles; // Size: 8
    uint32 m_nTickBase; 
    CHandle< C_BasePlayerPawn > m_hPawn; 
    char m_pad3_1588[3];
    bool m_bKnownTeamMismatch; 
    CHandle< C_BasePlayerPawn > m_hPredictedPawn; 
    CSplitScreenSlot m_nSplitScreenSlot; 
    CHandle< CBasePlayerController > m_hSplitOwner; 
    CUtlVector< CHandle< CBasePlayerController > > m_hSplitScreenPlayers; // Size: 24
    char m_pad3_1628[3];
    bool m_bIsHLTV; 
    PlayerConnectedState m_iConnected; 
    char[128] m_iszPlayerName; // Size: 136
    uint64 m_steamID; // Size: 8
    char m_pad3_1780[3];
    bool m_bIsLocalPlayerController; 
    uint32 m_iDesiredFOV; 
};

struct __declspec(align(8))  CLogicalEntity {
};

struct  C_BaseFlex::Emphasized_Phoneme {
    CUtlString m_sClassName; // Size: 24
    char m_pad[24];
    float32 m_flAmount; 
    bool m_bRequired; 
    bool m_bBasechecked; 
    bool m_bValid; 
};

struct  C_EnvWindShared {
    char m_pad[8];
    GameTime_t m_flStartTime; 
    uint32 m_iWindSeed; 
    uint16 m_iMinWind; 
    uint16 m_iMaxWind; 
    int32 m_windRadius; 
    uint16 m_iMinGust; 
    uint16 m_iMaxGust; 
    float32 m_flMinGustDelay; 
    float32 m_flMaxGustDelay; 
    float32 m_flGustDuration; 
    char m_pad2_44[2];
    uint16 m_iGustDirChange; 
    Vector m_location; // Size: 12
    int32 m_iszGustSound; 
    int32 m_iWindDir; 
    float32 m_flWindSpeed; 
    Vector m_currentWindVector; // Size: 12
    Vector m_CurrentSwayVector; // Size: 12
    Vector m_PrevSwayVector; // Size: 12
    char m_pad2_108[2];
    uint16 m_iInitialWindDir; 
    float32 m_flInitialWindSpeed; 
    GameTime_t m_flVariationTime; 
    GameTime_t m_flSwayTime; 
    GameTime_t m_flSimTime; 
    GameTime_t m_flSwitchTime; 
    float32 m_flAveWindSpeed; 
    char m_pad3_136[3];
    bool m_bGusting; 
    float32 m_flWindAngleVariation; 
    float32 m_flWindSpeedVariation; 
    CHandle< C_BaseEntity > m_hEntOwner; 
};

struct __declspec(align(8))  C_EnvWindClientside {
    char m_pad[1384];
    C_EnvWindShared m_EnvWindShared; 
};

struct __declspec(align(8))  C_EntityFlame {
    char m_pad[1384];
    CHandle< C_BaseEntity > m_hEntAttached; // Size: 40
    CHandle< C_BaseEntity > m_hOldAttached; 
    bool m_bCheapEffect; 
};

struct  CProjectedTextureBase {
    char m_pad[12];
    CHandle< C_BaseEntity > m_hTargetEntity; 
    bool m_bState; 
    char m_pad2_20[2];
    bool m_bAlwaysUpdate; 
    float32 m_flLightFOV; 
    bool m_bEnableShadows; 
    bool m_bSimpleProjection; 
    bool m_bLightOnlyTarget; 
    bool m_bLightWorld; 
    char m_pad3_32[3];
    bool m_bCameraSpace; 
    float32 m_flBrightnessScale; 
    Color m_LightColor; 
    float32 m_flIntensity; 
    float32 m_flLinearAttenuation; 
    float32 m_flQuadraticAttenuation; 
    char m_pad3_56[3];
    bool m_bVolumetric; 
    float32 m_flVolumetricIntensity; 
    float32 m_flNoiseStrength; 
    float32 m_flFlashlightTime; 
    uint32 m_nNumPlanes; 
    float32 m_flPlaneOffset; 
    float32 m_flColorTransitionTime; 
    float32 m_flAmbient; 
    char[512] m_SpotlightTextureName; // Size: 512
    int32 m_nSpotlightTextureFrame; 
    uint32 m_nShadowQuality; 
    float32 m_flNearZ; 
    float32 m_flFarZ; 
    float32 m_flProjectionSize; 
    float32 m_flRotation; 
    bool m_bFlipHorizontal; 
};

struct __declspec(align(8))  C_BaseFire {
    char m_pad[1384];
    float32 m_flScale; 
    float32 m_flStartScale; 
    float32 m_flScaleTime; 
    uint32 m_nFlags; 
};

struct  TimedEvent {
    float32 m_TimeBetweenEvents; 
    char m_pad[4];
    float32 m_fNextEvent; 
};

struct  CFireOverlay {
    char m_pad[208];
    C_FireSmoke* m_pOwner; // Size: 8
    Vector[4] m_vBaseColors; // Size: 48
    float32 m_flScale; 
    int32 m_nGUID; 
};

struct __declspec(align(8))  C_FireSmoke {
    char m_pad[1400];
    int32 m_nFlameModelIndex; 
    int32 m_nFlameFromAboveModelIndex; 
    float32 m_flScaleRegister; 
    float32 m_flScaleStart; 
    float32 m_flScaleEnd; 
    GameTime_t m_flScaleTimeStart; 
    GameTime_t m_flScaleTimeEnd; 
    char m_pad16_1448[16];
    float32 m_flChildFlameSpread; // Size: 20
    float32 m_flClipPerc; 
    bool m_bClipTested; 
    char m_pad2_1456[2];
    bool m_bFadingOut; 
    TimedEvent m_tParticleSpawn; // Size: 8
    CFireOverlay* m_pFireOverlay; 
};

struct __declspec(align(8))  C_RopeKeyframe {
    char m_pad[3376];
    CBitVec< 10 > m_LinksTouchingSomething; 
    int32 m_nLinksTouchingSomething; 
    char m_pad3_3388[3];
    bool m_bApplyWind; 
    int32 m_fPrevLockedPoints; 
    int32 m_iForcePointMoveCounter; 
    bool[2] m_bPrevEndPointPos; 
    Vector[2] m_vPrevEndPointPos; // Size: 24
    float32 m_flCurScroll; 
    float32 m_flScrollSpeed; 
    char m_pad6_3440[6];
    uint16 m_RopeFlags; // Size: 8
    CStrongHandle< InfoForResourceTypeIMaterial2 > m_iRopeMaterialModelIndex; // Size: 632
    Vector[10] m_LightValues; // Size: 120
    char m_pad3_4196[3];
    uint8 m_nSegments; 
    CHandle< C_BaseEntity > m_hStartPoint; 
    CHandle< C_BaseEntity > m_hEndPoint; 
    AttachmentHandle_t m_iStartAttachment; 
    AttachmentHandle_t m_iEndAttachment; 
    char m_pad1_4208[1];
    uint8 m_Subdiv; 
    int16 m_RopeLength; 
    int16 m_Slack; 
    float32 m_TextureScale; 
    uint8 m_fLockedPoints; 
    char m_pad2_4220[2];
    uint8 m_nChangeCount; 
    float32 m_Width; 
    C_RopeKeyframe::CPhysicsDelegate m_PhysicsDelegate; // Size: 16
    CStrongHandle< InfoForResourceTypeIMaterial2 > m_hMaterial; // Size: 8
    int32 m_TextureHeight; 
    Vector m_vecImpulse; // Size: 12
    Vector m_vecPreviousImpulse; // Size: 12
    float32 m_flCurrentGustTimer; 
    float32 m_flCurrentGustLifetime; 
    float32 m_flTimeToNextGust; 
    Vector m_vWindDir; // Size: 12
    Vector m_vColorMod; // Size: 12
    Vector[2] m_vCachedEndPointAttachmentPos; // Size: 24
    QAngle[2] m_vCachedEndPointAttachmentAngle; // Size: 24
    bool m_bConstrainBetweenEndpoints; 
    bitfield:1 m_bEndPointAttachmentPositionsDirty; 
    bitfield:1 m_bEndPointAttachmentAnglesDirty; 
    bitfield:1 m_bNewDataThisFrame; 
    bitfield:1 m_bPhysicsInitted; 
};

struct  C_RopeKeyframe::CPhysicsDelegate {
    char m_pad[8];
    C_RopeKeyframe* m_pKeyframe; 
};

struct  C_SceneEntity::QueuedEvents_t {
    float32 starttime; 
};

struct __declspec(align(8))  C_TintController {
};

struct  CFlashlightEffect {
    char m_pad[16];
    char m_pad15_32[15];
    bool m_bIsOn; // Size: 16
    char m_pad3_36[3];
    bool m_bMuzzleFlashEnabled; 
    char m_pad8_48[8];
    float32 m_flMuzzleFlashBrightness; // Size: 12
    Quaternion m_quatMuzzleFlashOrientation; // Size: 16
    Vector m_vecMuzzleFlashOrigin; // Size: 12
    float32 m_flFov; 
    float32 m_flFarZ; 
    float32 m_flLinearAtten; 
    char m_pad3_92[3];
    bool m_bCastsShadows; 
    float32 m_flCurrentPullBackDist; 
    CStrongHandle< InfoForResourceTypeCTextureBase > m_FlashlightTexture; // Size: 8
    CStrongHandle< InfoForResourceTypeCTextureBase > m_MuzzleFlashTexture; // Size: 8
    char[64] m_textureName; 
};

struct  CInterpolatedValue {
    float32 m_flStartTime; 
    char m_pad[4];
    float32 m_flEndTime; 
    float32 m_flStartValue; 
    float32 m_flEndValue; 
    int32 m_nInterpType; 
};

struct  CGlowSprite {
    Vector m_vColor; // Size: 12
    char m_pad[12];
    float32 m_flHorzSize; 
    char m_pad4_24[4];
    float32 m_flVertSize; // Size: 8
    CStrongHandle< InfoForResourceTypeIMaterial2 > m_hMaterial; 
};

struct  CGlowOverlay {
    char m_pad[8];
    Vector m_vPos; // Size: 12
    char m_pad3_24[3];
    bool m_bDirectional; 
    Vector m_vDirection; // Size: 12
    char m_pad3_40[3];
    bool m_bInSky; 
    char m_pad4_48[4];
    float32 m_skyObstructionScale; // Size: 8
    CGlowSprite[4] m_Sprites; // Size: 128
    int32 m_nSprites; 
    float32 m_flProxyRadius; 
    float32 m_flHDRColorScale; 
    float32 m_flGlowObstructionScale; 
    bool m_bCacheGlowObstruction; 
    bool m_bCacheSkyObstruction; 
    int16 m_bActivated; 
    char m_pad2_200[2];
    uint16 m_ListIndex; 
    int32 m_queryHandle; 
};

struct  IClientAlphaProperty {
};

struct __declspec(align(8))  C_SkyCamera {
    char m_pad[1384];
    sky3dparams_t m_skyboxData; // Size: 144
    CUtlStringToken m_skyboxSlotToken; 
    char m_pad3_1536[3];
    bool m_bUseAngles; 
    C_SkyCamera* m_pNext; 
};

struct __declspec(align(8))  CSkyboxReference {
    char m_pad[1384];
    WorldGroupId_t m_worldGroupId; 
    CHandle< C_SkyCamera > m_hSkyCamera; 
};

struct  sky3dparams_t {
    char m_pad[8];
    char m_pad2_12[2];
    int16 scale; 
    Vector origin; // Size: 12
    char m_pad3_28[3];
    bool bClip3DSkyBoxNearToWorldFar; 
    float32 flClip3DSkyBoxNearToWorldFarOffset; 
    fogparams_t fog; // Size: 104
    WorldGroupId_t m_nWorldGroupID; 
};

struct  VPhysicsCollisionAttribute_t {
    char m_pad[8];
    uint64 m_nInteractsAs; // Size: 8
    uint64 m_nInteractsWith; // Size: 8
    uint64 m_nInteractsExclude; // Size: 8
    uint32 m_nEntityId; 
    uint32 m_nOwnerId; 
    uint16 m_nHierarchyId; 
    uint8 m_nCollisionGroup; 
    uint8 m_nCollisionFunctionMask; 
};

struct  CDecalInfo {
    float32 m_flAnimationScale; 
    char m_pad[4];
    float32 m_flAnimationLifeSpan; 
    float32 m_flPlaceTime; 
    float32 m_flFadeStartTime; 
    float32 m_flFadeDuration; 
    int32 m_nVBSlot; 
    char m_pad12_40[12];
    int32 m_nBoneIndex; // Size: 16
    Vector m_vPosition; // Size: 12
    char m_pad8_64[8];
    float32 m_flBoundingRadiusSqr; // Size: 12
    CDecalInfo* m_pNext; // Size: 8
    CDecalInfo* m_pPrev; // Size: 136
    int32 m_nDecalMaterialIndex; 
};

struct  CEffectData {
    char m_pad[8];
    Vector m_vOrigin; // Size: 12
    Vector m_vStart; // Size: 12
    Vector m_vNormal; // Size: 12
    QAngle m_vAngles; // Size: 12
    CEntityHandle m_hEntity; 
    CEntityHandle m_hOtherEntity; 
    float32 m_flScale; 
    float32 m_flMagnitude; 
    float32 m_flRadius; 
    CUtlStringToken m_nSurfaceProp; 
    CWeakHandle< InfoForResourceTypeIParticleSystemDefinition > m_nEffectIndex; // Size: 8
    uint32 m_nDamageType; 
    char m_pad1_94[1];
    uint8 m_nPenetrate; 
    uint16 m_nMaterial; 
    uint16 m_nHitBox; 
    uint8 m_nColor; 
    uint8 m_fFlags; 
    AttachmentHandle_t m_nAttachmentIndex; 
    CUtlStringToken m_nAttachmentName; 
    uint16 m_iEffectName; 
    uint8 m_nExplosionType; 
};

struct __declspec(align(8))  C_EnvDetailController {
    char m_pad[1384];
    float32 m_flFadeStartDist; 
    float32 m_flFadeEndDist; 
};

struct  C_EnvWindShared::WindAveEvent_t {
    float32 m_flStartWindSpeed; 
    char m_pad[4];
    float32 m_flAveWindSpeed; 
};

struct  C_EnvWindShared::WindVariationEvent_t {
    float32 m_flWindAngleVariation; 
    char m_pad[4];
    float32 m_flWindSpeedVariation; 
};

struct __declspec(align(8))  C_InfoLadderDismount {
};

struct  shard_model_desc_t {
    char m_pad[8];
    char m_pad4_16[4];
    int32 m_nModelID; // Size: 8
    CStrongHandle< InfoForResourceTypeIMaterial2 > m_hMaterialBase; // Size: 8
    CStrongHandle< InfoForResourceTypeIMaterial2 > m_hMaterialDamageOverlay; // Size: 8
    ShardSolid_t m_solid; 
    Vector2D m_vecPanelSize; // Size: 8
    Vector2D m_vecStressPositionA; // Size: 8
    Vector2D m_vecStressPositionB; // Size: 12
    C_NetworkUtlVectorBase< Vector2D > m_vecPanelVertices; // Size: 24
    C_NetworkUtlVectorBase< Vector4D > m_vInitialPanelVertices; // Size: 24
    float32 m_flGlassHalfThickness; 
    bool m_bHasParent; 
    char m_pad2_120[2];
    bool m_bParentFrozen; 
    CUtlStringToken m_SurfacePropStringToken; 
};

struct __declspec(align(8))  C_GameRulesProxy {
};

struct  C_GameRules {
    char m_pad[8];
    CNetworkVarChainer __m_pChainEntity; // Size: 40
    int32 m_nTotalPausedTicks; 
    int32 m_nPauseStartTick; 
    bool m_bGamePaused; 
};

struct  CGlowProperty {
    char m_pad[8];
    Vector m_fGlowColor; // Size: 40
    int32 m_iGlowType; 
    int32 m_iGlowTeam; 
    int32 m_nGlowRange; 
    int32 m_nGlowRangeMin; 
    Color m_glowColorOverride; 
    char m_pad3_72[3];
    bool m_bFlashing; 
    float32 m_flGlowTime; 
    float32 m_flGlowStartTime; 
    bool m_bEligibleForScreenHighlight; 
    bool m_bGlowing; 
};

struct  C_MultiplayRules {
};

struct __declspec(align(8))  PhysicsRagdollPose_t {
    char m_pad[8];
    C_NetworkUtlVectorBase< CTransform > m_Transforms; // Size: 24
    CHandle< C_BaseEntity > m_hOwner; 
};

struct  C_SingleplayRules {
};

struct __declspec(align(8))  C_SoundOpvarSetPointBase {
    char m_pad[1384];
    CUtlSymbolLarge m_iszStackName; // Size: 8
    CUtlSymbolLarge m_iszOperatorName; // Size: 8
    CUtlSymbolLarge m_iszOpvarName; // Size: 8
    int32 m_iOpvarIndex; 
    bool m_bUseAutoCompare; 
};

struct __declspec(align(8))  C_SoundOpvarSetPointEntity {
};

struct __declspec(align(8))  C_SoundOpvarSetAABBEntity {
};

struct __declspec(align(8))  C_SoundOpvarSetOBBEntity {
};

struct __declspec(align(8))  C_SoundOpvarSetPathCornerEntity {
};

struct __declspec(align(8))  C_SoundOpvarSetAutoRoomEntity {
};

struct __declspec(align(8))  C_SoundOpvarSetOBBWindEntity {
};

struct  C_TeamplayRules {
};

struct __declspec(align(8))  C_TeamRoundTimer {
    char m_pad[1384];
    char m_pad3_1388[3];
    bool m_bTimerPaused; 
    float32 m_flTimeRemaining; 
    GameTime_t m_flTimerEndTime; 
    bool m_bIsDisabled; 
    char m_pad2_1400[2];
    bool m_bShowInHUD; 
    int32 m_nTimerLength; 
    int32 m_nTimerInitialLength; 
    int32 m_nTimerMaxLength; 
    char m_pad3_1416[3];
    bool m_bAutoCountdown; 
    int32 m_nSetupTimeLength; 
    int32 m_nState; 
    bool m_bStartPaused; 
    char m_pad2_1428[2];
    bool m_bInCaptureWatchState; 
    float32 m_flTotalTime; 
    bool m_bStopWatchTimer; 
    bool m_bFireFinished; 
    bool m_bFire5MinRemain; 
    bool m_bFire4MinRemain; 
    bool m_bFire3MinRemain; 
    bool m_bFire2MinRemain; 
    bool m_bFire1MinRemain; 
    bool m_bFire30SecRemain; 
    bool m_bFire10SecRemain; 
    bool m_bFire5SecRemain; 
    bool m_bFire4SecRemain; 
    bool m_bFire3SecRemain; 
    bool m_bFire2SecRemain; 
    char m_pad2_1448[2];
    bool m_bFire1SecRemain; 
    int32 m_nOldTimerLength; 
    int32 m_nOldTimerState; 
};

struct __declspec(align(8))  C_PortraitWorldCallbackHandler {
};

struct  CEconItemAttribute {
    char m_pad[48];
    char m_pad2_52[2];
    uint16 m_iAttributeDefinitionIndex; 
    float32 m_flValue; 
    float32 m_flInitialValue; 
    int32 m_nRefundableCurrency; 
    bool m_bSetBonus; 
};

struct  CAttributeManager {
    char m_pad[8];
    CUtlVector< CHandle< C_BaseEntity > > m_Providers; // Size: 24
    int32 m_iReapplyProvisionParity; 
    CHandle< C_BaseEntity > m_hOuter; 
    char m_pad3_44[3];
    bool m_bPreventLoopback; 
    attributeprovidertypes_t m_ProviderType; 
    CUtlVector< CAttributeManager::cached_attribute_float_t > m_CachedResults; 
};

struct  CAttributeList {
    char m_pad[8];
    C_UtlVectorEmbeddedNetworkVar< CEconItemAttribute > m_Attributes; // Size: 80
    CAttributeManager* m_pManager; 
};

struct  CAttributeManager::cached_attribute_float_t {
    char m_pad4_8[4];
    float32 flIn; // Size: 8
    char m_pad[8];
    CUtlSymbolLarge iAttribHook; // Size: 8
    float32 flOut; 
};

struct  C_EconItemView {
    char m_pad[96];
    bool m_bInventoryImageRgbaRequested; 
    char m_pad30_128[30];
    bool m_bInventoryImageTriedCache; // Size: 31
    int32 m_nInventoryImageRgbaWidth; 
    int32 m_nInventoryImageRgbaHeight; 
    char[260] m_szCurrentLoadCachedFileName; // Size: 304
    char m_pad1_442[1];
    bool m_bRestoreCustomMaterialAfterPrecache; 
    uint16 m_iItemDefinitionIndex; 
    int32 m_iEntityQuality; 
    char m_pad4_456[4];
    uint32 m_iEntityLevel; // Size: 8
    uint64 m_iItemID; // Size: 8
    uint32 m_iItemIDHigh; 
    uint32 m_iItemIDLow; 
    uint32 m_iAccountID; 
    char m_pad8_488[8];
    uint32 m_iInventoryPosition; // Size: 12
    bool m_bInitialized; 
    bool m_bDisallowSOC; 
    bool m_bIsStoreItem; 
    bool m_bIsTradeItem; 
    int32 m_iEntityQuantity; 
    int32 m_iRarityOverride; 
    int32 m_iQualityOverride; 
    int32 m_iOriginOverride; 
    uint8 m_unClientFlags; 
    char m_pad18_528[18];
    uint8 m_unOverrideStyle; // Size: 19
    CAttributeList m_AttributeList; // Size: 96
    CAttributeList m_NetworkedDynamicAttributes; // Size: 96
    char[161] m_szCustomName; // Size: 161
    char[161] m_szCustomNameOverride; // Size: 207
    bool m_bInitializedTags; 
};

struct  C_AttributeContainer {
    char m_pad[80];
    C_EconItemView m_Item; // Size: 1096
    char m_pad4_1184[4];
    int32 m_iExternalItemProviderRegisteredToken; // Size: 8
    uint64 m_ullRegisteredAsItemID; 
};

struct  C_EconEntity::AttachedModelData_t {
    int32 m_iModelDisplayFlags; 
};

struct  EntitySpottedState_t {
    char m_pad[8];
    char m_pad3_12[3];
    bool m_bSpotted; 
    uint32[2] m_bSpottedByMask; 
};

struct  C_CSGameRules {
    char m_pad[64];
    bool m_bFreezePeriod; 
    char m_pad2_68[2];
    bool m_bWarmupPeriod; 
    GameTime_t m_fWarmupPeriodEnd; 
    GameTime_t m_fWarmupPeriodStart; 
    bool m_bServerPaused; 
    bool m_bTerroristTimeOutActive; 
    char m_pad1_80[1];
    bool m_bCTTimeOutActive; 
    float32 m_flTerroristTimeOutRemaining; 
    float32 m_flCTTimeOutRemaining; 
    int32 m_nTerroristTimeOuts; 
    int32 m_nCTTimeOuts; 
    bool m_bTechnicalTimeOut; 
    char m_pad2_100[2];
    bool m_bMatchWaitingForResume; 
    int32 m_iRoundTime; 
    float32 m_fMatchStartTime; 
    GameTime_t m_fRoundStartTime; 
    GameTime_t m_flRestartRoundTime; 
    char m_pad3_120[3];
    bool m_bGameRestart; 
    float32 m_flGameStartTime; 
    float32 m_timeUntilNextPhaseStarts; 
    int32 m_gamePhase; 
    int32 m_totalRoundsPlayed; 
    int32 m_nRoundsPlayedThisPhase; 
    int32 m_nOvertimePlaying; 
    int32 m_iHostagesRemaining; 
    bool m_bAnyHostageReached; 
    bool m_bMapHasBombTarget; 
    bool m_bMapHasRescueZone; 
    bool m_bMapHasBuyZone; 
    char m_pad3_156[3];
    bool m_bIsQueuedMatchmaking; 
    int32 m_nQueuedMatchmakingMode; 
    bool m_bIsValveDS; 
    bool m_bLogoMap; 
    char m_pad1_164[1];
    bool m_bPlayAllStepSoundsOnServer; 
    int32 m_iSpectatorSlotCount; 
    int32 m_MatchDevice; 
    char m_pad3_176[3];
    bool m_bHasMatchStarted; 
    int32 m_nNextMapInMapgroup; 
    char[512] m_szTournamentEventName; // Size: 512
    char[512] m_szTournamentEventStage; // Size: 512
    char[512] m_szMatchStatTxt; // Size: 512
    char[512] m_szTournamentPredictionsTxt; // Size: 512
    int32 m_nTournamentPredictionsPct; 
    GameTime_t m_flCMMItemDropRevealStartTime; 
    GameTime_t m_flCMMItemDropRevealEndTime; 
    bool m_bIsDroppingItems; 
    bool m_bIsQuestEligible; 
    char m_pad1_2244[1];
    bool m_bIsHltvActive; 
    uint16[100] m_arrProhibitedItemIndices; // Size: 200
    uint32[4] m_arrTournamentActiveCasterAccounts; // Size: 16
    int32 m_numBestOfMaps; 
    int32 m_nHalloweenMaskListSeed; 
    bool m_bBombDropped; 
    char m_pad2_2472[2];
    bool m_bBombPlanted; 
    int32 m_iRoundWinStatus; 
    int32 m_eRoundWinReason; 
    bool m_bTCantBuy; 
    char m_pad2_2484[2];
    bool m_bCTCantBuy; 
    int32[30] m_iMatchStats_RoundResults; // Size: 120
    int32[30] m_iMatchStats_PlayersAlive_CT; // Size: 120
    int32[30] m_iMatchStats_PlayersAlive_T; // Size: 120
    float32[32] m_TeamRespawnWaveTimes; // Size: 128
    GameTime_t[32] m_flNextRespawnWave; // Size: 128
    int32 m_nServerQuestID; 
    Vector m_vMinimapMins; // Size: 12
    Vector m_vMinimapMaxs; // Size: 12
    float32[8] m_MinimapVerticalSectionHeights; // Size: 32
    char m_pad3_3164[3];
    bool m_bSpawnedTerrorHuntHeavy; 
    int32[10] m_nEndMatchMapGroupVoteTypes; // Size: 40
    int32[10] m_nEndMatchMapGroupVoteOptions; // Size: 40
    int32 m_nEndMatchMapVoteWinner; 
    int32 m_iNumConsecutiveCTLoses; 
    char m_pad24_3280[24];
    int32 m_iNumConsecutiveTerroristLoses; // Size: 28
    char m_pad167_3448[167];
    bool m_bMarkClientStopRecordAtRoundEnd; // Size: 168
    int32 m_nMatchAbortedEarlyReason; 
    bool m_bHasTriggeredRoundStartMusic; 
    char m_pad26_3480[26];
    bool m_bSwitchingTeamsAtRoundReset; // Size: 27
    CCSGameModeRules* m_pGameModeRules; // Size: 8
    C_RetakeGameRules m_RetakeRules; // Size: 280
    char m_pad3_3772[3];
    uint8 m_nMatchEndCount; 
    int32 m_nTTeamIntroVariant; 
    int32 m_nCTTeamIntroVariant; 
    char m_pad3_3784[3];
    bool m_bTeamIntroPeriod; 
    int32 m_iRoundEndWinnerTeam; 
    int32 m_eRoundEndReason; 
    char m_pad3_3796[3];
    bool m_bRoundEndShowTimerDefend; 
    int32 m_iRoundEndTimerTime; 
    CUtlString m_sRoundEndFunFactToken; // Size: 8
    CPlayerSlot m_iRoundEndFunFactPlayerSlot; 
    int32 m_iRoundEndFunFactData1; 
    int32 m_iRoundEndFunFactData2; 
    int32 m_iRoundEndFunFactData3; 
    CUtlString m_sRoundEndMessage; // Size: 8
    int32 m_iRoundEndPlayerCount; 
    char m_pad3_3840[3];
    bool m_bRoundEndNoMusic; 
    int32 m_iRoundEndLegacy; 
    char m_pad3_3848[3];
    uint8 m_nRoundEndCount; 
    int32 m_iRoundStartRoundNumber; 
    char m_pad16395_20248[16395];
    uint8 m_nRoundStartCount; // Size: 16396
    float64 m_flLastPerfSampleTime; 
};

struct __declspec(align(8))  C_CSGameRulesProxy {
    char m_pad[1384];
    C_CSGameRules* m_pGameRules; 
};

struct __declspec(align(8))  CCSGameModeRules {
    char m_pad[8];
    CNetworkVarChainer __m_pChainEntity; 
};

struct  C_RetakeGameRules {
    char m_pad[248];
    int32 m_nMatchSeed; 
    bool m_bBlockersPresent; 
    char m_pad2_256[2];
    bool m_bRoundInProgress; 
    int32 m_iFirstSecondHalfRound; 
    int32 m_iBombSite; 
};

struct __declspec(align(8))  CCSGameModeRules_Noop {
};

struct __declspec(align(8))  CCSGameModeRules_ArmsRace {
    char m_pad[48];
    C_NetworkUtlVectorBase< CUtlString > m_WeaponSequence; 
};

struct __declspec(align(8))  CCSGameModeRules_Deathmatch {
    char m_pad[48];
    GameTime_t m_flDMBonusStartTime; 
    float32 m_flDMBonusTimeLength; 
    CUtlString m_sDMBonusWeapon; 
};

struct  CSPerRoundStats_t {
    char m_pad[48];
    int32 m_iKills; 
    int32 m_iDeaths; 
    int32 m_iAssists; 
    int32 m_iDamage; 
    int32 m_iEquipmentValue; 
    int32 m_iMoneySaved; 
    int32 m_iKillReward; 
    int32 m_iLiveTime; 
    int32 m_iHeadShotKills; 
    int32 m_iObjective; 
    int32 m_iCashEarned; 
    int32 m_iUtilityDamage; 
    int32 m_iEnemiesFlashed; 
};

struct  CSMatchStats_t {
    char m_pad[104];
    int32 m_iEnemy5Ks; 
    int32 m_iEnemy4Ks; 
    int32 m_iEnemy3Ks; 
    int32 m_iEnemyKnifeKills; 
    int32 m_iEnemyTaserKills; 
};

struct  C_CSGO_TeamPreviewCharacterPosition {
    char m_pad[1384];
    int32 m_nVariant; 
    int32 m_nRandom; 
    char m_pad4_1400[4];
    int32 m_nOrdinal; // Size: 8
    CUtlString m_sWeaponName; // Size: 8
    uint64 m_xuid; // Size: 8
    C_EconItemView m_agentItem; // Size: 1096
    C_EconItemView m_glovesItem; // Size: 1096
    C_EconItemView m_weaponItem; 
};

struct  C_CSGO_TeamSelectCharacterPosition {
};

struct __declspec(align(8))  C_CSGO_TeamSelectTerroristPosition {
};

struct __declspec(align(8))  C_CSGO_TeamSelectCounterTerroristPosition {
};

struct  C_CSGO_TeamIntroCharacterPosition {
};

struct __declspec(align(8))  C_CSGO_TeamIntroTerroristPosition {
};

struct __declspec(align(8))  C_CSGO_TeamIntroCounterTerroristPosition {
};

struct  CCSGO_WingmanIntroCharacterPosition {
};

struct __declspec(align(8))  CCSGO_WingmanIntroTerroristPosition {
};

struct __declspec(align(8))  CCSGO_WingmanIntroCounterTerroristPosition {
};

struct __declspec(align(8))  C_CSMinimapBoundary {
};

struct __declspec(align(8))  CCSPointScriptEntity {
};

struct __declspec(align(8))  CCSClientPointScriptEntity {
};

struct  CCSPointScript {
    char m_pad[248];
    CCSPointScriptEntity* m_pParent; 
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
    GameTick_t nTagTick; 
    float32 flFlinchModSmall; 
    float32 flFlinchModLarge; 
    float32 flFriendlyFireDamageReductionRatio; 
};

struct __declspec(align(16))  C_CSPlayerPawn {
    char m_pad[5400];
    CCSPlayer_BulletServices* m_pBulletServices; // Size: 8
    CCSPlayer_HostageServices* m_pHostageServices; // Size: 8
    CCSPlayer_BuyServices* m_pBuyServices; // Size: 8
    CCSPlayer_GlowServices* m_pGlowServices; // Size: 8
    CCSPlayer_ActionTrackingServices* m_pActionTrackingServices; // Size: 8
    CCSPlayer_DamageReactServices* m_pDamageReactServices; // Size: 8
    GameTime_t m_flHealthShotBoostExpirationTime; 
    GameTime_t m_flLastFiredWeaponTime; 
    char m_pad3_5460[3];
    bool m_bHasFemaleVoice; 
    float32 m_flLandingTimeSeconds; 
    float32 m_flOldFallVelocity; 
    char[18] m_szLastPlaceName; // Size: 18
    bool m_bPrevDefuser; 
    bool m_bPrevHelmet; 
    int32 m_nPrevArmorVal; 
    int32 m_nPrevGrenadeAmmoCount; 
    uint32 m_unPreviousWeaponHash; 
    uint32 m_unWeaponHash; 
    bool m_bInBuyZone; 
    char m_pad2_5508[2];
    bool m_bPreviouslyInBuyZone; 
    QAngle m_aimPunchAngle; // Size: 12
    QAngle m_aimPunchAngleVel; // Size: 12
    int32 m_aimPunchTickBase; 
    char m_pad4_5544[4];
    float32 m_aimPunchTickFraction; // Size: 8
    CUtlVector< QAngle > m_aimPunchCache; // Size: 32
    char m_pad3_5580[3];
    bool m_bInLanding; 
    float32 m_flLandingStartTime; 
    bool m_bInHostageRescueZone; 
    bool m_bInBombZone; 
    char m_pad1_5588[1];
    bool m_bIsBuyMenuOpen; 
    GameTime_t m_flTimeOfLastInjury; 
    GameTime_t m_flNextSprayDecalTime; // Size: 312
    int32 m_iRetakesOffering; 
    int32 m_iRetakesOfferingCard; 
    bool m_bRetakesHasDefuseKit; 
    char m_pad2_5916[2];
    bool m_bRetakesMVPLastRound; 
    int32 m_iRetakesMVPBoostItem; 
    loadout_slot_t m_RetakesMVPBoostExtraUtility; // Size: 32
    char m_pad7_5960[7];
    bool m_bNeedToReApplyGloves; // Size: 8
    C_EconItemView m_EconGloves; // Size: 1096
    uint8 m_nEconGlovesChanged; 
    char m_pad2_7060[2];
    bool m_bMustSyncRagdollState; 
    int32 m_nRagdollDamageBone; 
    Vector m_vRagdollDamageForce; // Size: 12
    Vector m_vRagdollDamagePosition; // Size: 12
    char[64] m_szRagdollDamageWeaponName; // Size: 64
    char m_pad3_7156[3];
    bool m_bRagdollDamageHeadshot; 
    Vector m_vRagdollServerOrigin; // Size: 1668
    char m_pad3_8828[3];
    bool m_bLastHeadBoneTransformIsValid; 
    GameTime_t m_lastLandTime; 
    char m_pad27_8860[27];
    bool m_bOnGroundLastTick; // Size: 28
    QAngle m_qDeathEyeAngles; // Size: 12
    bool m_bSkipOneHeadConstraintUpdate; 
    char m_pad2_8876[2];
    bool m_bLeftHanded; 
    GameTime_t m_fSwitchedHandednessTime; 
    float32 m_flViewmodelOffsetX; 
    float32 m_flViewmodelOffsetY; 
    float32 m_flViewmodelOffsetZ; 
    float32 m_flViewmodelFOV; 
    uint32[5] m_vecPlayerPatchEconIndices; // Size: 56
    Color m_GunGameImmunityColor; // Size: 80
    CUtlVector< C_BulletHitModel* > m_vecBulletHitModels; // Size: 24
    char m_pad7_9064[7];
    bool m_bIsWalking; // Size: 8
    QAngle m_thirdPersonHeading; // Size: 24
    char m_pad12_9104[12];
    float32 m_flSlopeDropOffset; // Size: 16
    char m_pad12_9120[12];
    float32 m_flSlopeDropHeight; // Size: 16
    Vector m_vHeadConstraintOffset; // Size: 24
    EntitySpottedState_t m_entitySpottedState; // Size: 24
    bool m_bIsScoped; 
    bool m_bResumeZoom; 
    bool m_bIsDefusing; 
    bool m_bIsGrabbingHostage; 
    CSPlayerBlockingUseAction_t m_iBlockingUseActionInProgress; 
    GameTime_t m_flEmitSoundTime; 
    char m_pad3_9184[3];
    bool m_bInNoDefuseArea; 
    int32 m_nWhichBombZone; 
    int32 m_iShotsFired; 
    float32 m_flFlinchStack; 
    float32 m_flVelocityModifier; 
    float32 m_flHitHeading; 
    int32 m_nHitBodyPart; 
    char m_pad3_9212[3];
    bool m_bWaitForNoAttack; 
    char m_pad1_9217[1];
    float32 m_ignoreLadderJumpTime; 
    char m_pad2_9220[2];
    bool m_bKilledByHeadshot; 
    int32 m_ArmorValue; 
    uint16 m_unCurrentEquipmentValue; 
    uint16 m_unRoundStartEquipmentValue; 
    char m_pad2_9232[2];
    uint16 m_unFreezetimeEndEquipmentValue; 
    CEntityIndex m_nLastKillerIndex; 
    bool m_bOldIsScoped; 
    char m_pad2_9240[2];
    bool m_bHasDeathInfo; 
    float32 m_flDeathInfoTime; 
    Vector m_vecDeathInfoOrigin; // Size: 12
    GameTime_t m_grenadeParameterStashTime; 
    char m_pad3_9264[3];
    bool m_bGrenadeParametersStashed; 
    QAngle m_angStashedShootAngles; // Size: 12
    Vector m_vecStashedGrenadeThrowPosition; // Size: 12
    Vector m_vecStashedVelocity; // Size: 12
    QAngle[2] m_angShootAngleHistory; // Size: 24
    Vector[2] m_vecThrowPositionHistory; // Size: 24
    Vector[2] m_vecVelocityHistory; // Size: 28
    C_UtlVectorEmbeddedNetworkVar< PredictedDamageTag_t > m_PredictedDamageTags; // Size: 80
    GameTick_t m_nPrevHighestReceivedDamageTagTick; 
    int32 m_nHighestAppliedDamageTagTick; 
};

struct __declspec(align(8))  C_PlayerPing {
    char m_pad[1432];
    CHandle< C_CSPlayerPawn > m_hPlayer; 
    CHandle< C_BaseEntity > m_hPingedEntity; 
    int32 m_iType; 
    bool m_bUrgent; 
    char[18] m_szPlaceName; 
};

struct  CCSPlayer_PingServices {
    char m_pad[64];
    CHandle< C_BaseEntity > m_hPlayerPing; 
};

struct __declspec(align(8))  C_CSPlayerResource {
    char m_pad[1384];
    bool[12] m_bHostageAlive; // Size: 12
    bool[12] m_isHostageFollowingSomeone; // Size: 12
    CEntityIndex[12] m_iHostageEntityIDs; // Size: 48
    Vector m_bombsiteCenterA; // Size: 12
    Vector m_bombsiteCenterB; // Size: 12
    int32[4] m_hostageRescueX; // Size: 16
    int32[4] m_hostageRescueY; // Size: 16
    int32[4] m_hostageRescueZ; // Size: 16
    bool m_bEndMatchNextMapAllVoted; 
    bool m_foundGoalPositions; 
};

struct  CCSPlayer_DamageReactServices {
};

struct  CPlayer_ViewModelServices {
};

struct  CCSPlayerBase_CameraServices {
    char m_pad[528];
    uint32 m_iFOV; 
    uint32 m_iFOVStart; 
    GameTime_t m_flFOVTime; 
    float32 m_flFOVRate; 
    CHandle< C_BaseEntity > m_hZoomOwner; 
    float32 m_flLastShotFOV; 
};

struct  WeaponPurchaseCount_t {
    char m_pad[48];
    uint16 m_nItemDefIndex; 
    uint16 m_nCount; 
};

struct  WeaponPurchaseTracker_t {
    char m_pad[8];
    C_UtlVectorEmbeddedNetworkVar< WeaponPurchaseCount_t > m_weaponPurchases; 
};

struct  CCSPlayer_ActionTrackingServices {
    char m_pad[64];
    CHandle< C_BasePlayerWeapon > m_hLastWeaponBeforeC4AutoSwitch; 
    char m_pad3_72[3];
    bool m_bIsRescuing; 
    WeaponPurchaseTracker_t m_weaponPurchasesThisMatch; // Size: 88
    WeaponPurchaseTracker_t m_weaponPurchasesThisRound; 
};

struct  CCSPlayer_BulletServices {
    char m_pad[64];
    int32 m_totalHitsOnServer; 
};

struct  SellbackPurchaseEntry_t {
    char m_pad[48];
    char m_pad2_52[2];
    uint16 m_unDefIdx; 
    int32 m_nCost; 
    int32 m_nPrevArmor; 
    char m_pad3_64[3];
    bool m_bPrevHelmet; 
    CEntityHandle m_hItem; 
};

struct  CCSPlayer_BuyServices {
    char m_pad[64];
    C_UtlVectorEmbeddedNetworkVar< SellbackPurchaseEntry_t > m_vecSellbackPurchaseEntries; 
};

struct  CCSPlayer_CameraServices {
    char m_pad[552];
    char m_pad4_560[4];
    float32 m_flDeathCamTilt; // Size: 8
    Vector m_vClientScopeInaccuracy; 
};

struct  CCSPlayer_HostageServices {
    char m_pad[64];
    CHandle< C_BaseEntity > m_hCarriedHostage; 
    CHandle< C_BaseEntity > m_hCarriedHostageProp; 
};

struct  CCSPlayer_ItemServices {
    char m_pad[64];
    bool m_bHasDefuser; 
    bool m_bHasHelmet; 
    bool m_bHasHeavyArmor; 
};

struct  CCSPlayer_MovementServices {
    char m_pad[536];
    float32 m_flMaxFallVelocity; 
    Vector m_vecLadderNormal; // Size: 12
    int32 m_nLadderSurfacePropIndex; 
    float32 m_flDuckAmount; 
    float32 m_flDuckSpeed; 
    bool m_bDuckOverride; 
    char m_pad2_568[2];
    bool m_bDesiresDuck; 
    float32 m_flDuckOffset; 
    uint32 m_nDuckTimeMsecs; 
    uint32 m_nDuckJumpTimeMsecs; 
    uint32 m_nJumpTimeMsecs; 
    char m_pad12_600[12];
    float32 m_flLastDuckTime; // Size: 16
    Vector2D m_vecLastPositionAtFullCrouchSpeed; // Size: 8
    bool m_duckUntilOnGround; 
    bool m_bHasWalkMovedSinceLastJump; 
    char m_pad13_624[13];
    bool m_bInStuckTest; // Size: 14
    float32[64][2] m_flStuckCheckTime; // Size: 512
    int32 m_nTraceCount; 
    int32 m_StuckLast; 
    char m_pad3_1148[3];
    bool m_bSpeedCropped; 
    float32 m_flGroundMoveEfficiency; 
    int32 m_nOldWaterLevel; 
    float32 m_flWaterEntryTime; 
    Vector m_vecForward; // Size: 12
    Vector m_vecLeft; // Size: 12
    Vector m_vecUp; // Size: 12
    int32 m_nGameCodeHasMovedPlayerAfterCommand; 
    char m_pad3_1204[3];
    bool m_bOldJumpPressed; 
    float32 m_flJumpPressedTime; 
    float32 m_flJumpUntil; 
    float32 m_flJumpVel; 
    GameTime_t m_fStashGrenadeParameterWhen; // Size: 8
    uint64 m_nButtonDownMaskPrev; // Size: 8
    float32 m_flOffsetTickCompleteTime; 
    float32 m_flOffsetTickStashedSpeed; 
    float32 m_flStamina; 
    float32 m_flHeightAtJumpStart; 
    float32 m_flMaxJumpHeightThisJump; 
    float32 m_flMaxJumpHeightLastJump; 
};

struct  CCSPlayer_UseServices {
};

struct __declspec(align(8))  C_BaseViewModel {
    char m_pad[3984];
    Vector m_vecLastFacing; // Size: 12
    uint32 m_nViewModelIndex; 
    uint32 m_nAnimationParity; 
    float32 m_flAnimationStartTime; 
    CHandle< C_BasePlayerWeapon > m_hWeapon; // Size: 8
    CUtlSymbolLarge m_sVMName; // Size: 8
    CUtlSymbolLarge m_sAnimationPrefix; // Size: 8
    AttachmentHandle_t m_iCameraAttachment; 
    QAngle m_vecLastCameraAngles; // Size: 12
    float32 m_previousElapsedDuration; 
    float32 m_previousCycle; 
    int32 m_nOldAnimationParity; 
    HSequence m_hOldLayerSequence; 
    int32 m_oldLayer; 
    float32 m_oldLayerStartTime; 
    CHandle< C_BaseEntity > m_hControlPanel; 
};

struct  CCSPlayer_ViewModelServices {
    char m_pad[64];
    CHandle< C_BaseViewModel >[3] m_hViewModel; 
};

struct  CCSPlayer_WaterServices {
    char m_pad[64];
    float32 m_flWaterJumpTime; 
    Vector m_vecWaterJumpVel; // Size: 12
    float32 m_flSwimSoundTime; 
};

struct  CCSPlayer_WeaponServices {
    char m_pad[184];
    GameTime_t m_flNextAttack; 
    bool m_bIsLookingAtWeapon; 
    char m_pad2_192[2];
    bool m_bIsHoldingLookAtWeapon; 
    char m_pad916_1112[916];
    uint32 m_nOldShootPositionHistoryCount; // Size: 920
    uint32 m_nOldInputHistoryCount; 
};

struct  CCSObserver_ObserverServices {
    char m_pad[88];
    CEntityHandle m_hLastObserverTarget; 
    Vector m_vecObserverInterpolateOffset; // Size: 12
    Vector m_vecObserverInterpStartPos; // Size: 12
    char m_pad8_128[8];
    float32 m_flObsInterp_PathLength; // Size: 12
    Quaternion m_qObsInterp_OrientationStart; // Size: 16
    Quaternion m_qObsInterp_OrientationTravelDir; // Size: 16
    ObserverInterpState_t m_obsInterpState; 
    bool m_bObserverInterpolationNeedsDeferredSetup; 
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
    C_UtlVectorEmbeddedNetworkVar< CSPerRoundStats_t > m_perRoundStats; // Size: 80
    CSMatchStats_t m_matchStats; // Size: 128
    int32 m_iNumRoundKills; 
    int32 m_iNumRoundKillsHeadshots; 
    uint32 m_unTotalRoundDamageDealt; 
};

struct __declspec(align(8))  CCSPlayerController {
    char m_pad[1824];
    CCSPlayerController_InGameMoneyServices* m_pInGameMoneyServices; // Size: 8
    CCSPlayerController_InventoryServices* m_pInventoryServices; // Size: 8
    CCSPlayerController_ActionTrackingServices* m_pActionTrackingServices; // Size: 8
    CCSPlayerController_DamageServices* m_pDamageServices; // Size: 8
    uint32 m_iPing; 
    char m_pad3_1864[3];
    bool m_bHasCommunicationAbuseMute; 
    CUtlSymbolLarge m_szCrosshairCodes; // Size: 8
    char m_pad3_1876[3];
    uint8 m_iPendingTeamNum; 
    GameTime_t m_flForceTeamTime; 
    int32 m_iCompTeammateColor; 
    char m_pad3_1888[3];
    bool m_bEverPlayedOnTeam; 
    GameTime_t m_flPreviousForceJoinTeamTime; // Size: 8
    CUtlSymbolLarge m_szClan; // Size: 8
    CUtlString m_sSanitizedPlayerName; // Size: 8
    char m_pad4_1920[4];
    int32 m_iCoachingTeam; // Size: 8
    uint64 m_nPlayerDominated; // Size: 8
    uint64 m_nPlayerDominatingMe; // Size: 8
    int32 m_iCompetitiveRanking; 
    int32 m_iCompetitiveWins; 
    char m_pad3_1948[3];
    int8 m_iCompetitiveRankType; 
    int32 m_iCompetitiveRankingPredicted_Win; 
    int32 m_iCompetitiveRankingPredicted_Loss; 
    int32 m_iCompetitiveRankingPredicted_Tie; 
    int32 m_nEndMatchNextMapVote; 
    char m_pad2_1968[2];
    uint16 m_unActiveQuestId; 
    QuestProgress::Reason m_nQuestProgressReason; 
    char m_pad40_2016[40];
    uint32 m_unPlayerTvControlFlags; // Size: 44
    int32 m_iDraftIndex; 
    uint32 m_msQueuedModeDisconnectionTimestamp; 
    uint32 m_uiAbandonRecordedReason; 
    bool m_bCannotBeKicked; 
    bool m_bEverFullyConnected; 
    bool m_bAbandonAllowsSurrender; 
    bool m_bAbandonOffersInstantSurrender; 
    bool m_bDisconnection1MinWarningPrinted; 
    char m_pad2_2036[2];
    bool m_bScoreReported; 
    char m_pad8_2048[8];
    int32 m_nDisconnectionTick; // Size: 12
    bool m_bControllingBot; 
    bool m_bHasControlledBotThisRound; 
    char m_pad1_2052[1];
    bool m_bHasBeenControlledByPlayerThisRound; 
    int32 m_nBotsControlledThisRound; 
    char m_pad3_2060[3];
    bool m_bCanControlObservedBot; 
    CHandle< C_CSPlayerPawn > m_hPlayerPawn; 
    CHandle< C_CSObserverPawn > m_hObserverPawn; 
    char m_pad3_2072[3];
    bool m_bPawnIsAlive; 
    uint32 m_iPawnHealth; 
    int32 m_iPawnArmor; 
    bool m_bPawnHasDefuser; 
    bool m_bPawnHasHelmet; 
    uint16 m_nPawnCharacterDefIndex; 
    int32 m_iPawnLifetimeStart; 
    int32 m_iPawnLifetimeEnd; 
    int32 m_iPawnBotDifficulty; 
    CHandle< CCSPlayerController > m_hOriginalControllerOfCurrentPawn; 
    int32 m_iScore; 
    C_NetworkUtlVectorBase< EKillTypes_t > m_vecKills; // Size: 24
    char m_pad3_2132[3];
    bool m_bMvpNoMusic; 
    int32 m_eMvpReason; 
    int32 m_iMusicKitID; 
    int32 m_iMusicKitMVPs; 
    int32 m_iMVPs; 
    bool m_bIsPlayerNameDirty; 
};

struct  CDamageRecord {
    char m_pad[40];
    CHandle< C_CSPlayerPawn > m_PlayerDamager; 
    CHandle< C_CSPlayerPawn > m_PlayerRecipient; 
    CHandle< CCSPlayerController > m_hPlayerControllerDamager; 
    CHandle< CCSPlayerController > m_hPlayerControllerRecipient; 
    CUtlString m_szPlayerDamagerName; // Size: 8
    CUtlString m_szPlayerRecipientName; // Size: 8
    uint64 m_DamagerXuid; // Size: 8
    uint64 m_RecipientXuid; // Size: 8
    int32 m_iBulletsDamage; 
    int32 m_iDamage; 
    int32 m_iActualHealthRemoved; 
    int32 m_iNumHits; 
    int32 m_iLastBulletUpdate; 
    bool m_bIsOtherEnemy; 
    EKillTypes_t m_killType; 
};

struct  CCSPlayerController_DamageServices {
    char m_pad[64];
    char m_pad4_72[4];
    int32 m_nSendUpdate; // Size: 8
    C_UtlVectorEmbeddedNetworkVar< CDamageRecord > m_DamageList; 
};

struct  CCSPlayerController_InGameMoneyServices {
    char m_pad[64];
    int32 m_iAccount; 
    int32 m_iStartAccount; 
    int32 m_iTotalCashSpent; 
    int32 m_iCashSpentThisRound; 
};

struct  ServerAuthoritativeWeaponSlot_t {
    char m_pad[40];
    uint16 unClass; 
    uint16 unSlot; 
    uint16 unItemDefIdx; 
};

struct  CCSPlayerController_InventoryServices {
    char m_pad[64];
    char m_pad2_68[2];
    uint16 m_unMusicID; 
    MedalRank_t[6] m_rank; // Size: 24
    int32 m_nPersonaDataPublicLevel; 
    int32 m_nPersonaDataPublicCommendsLeader; 
    int32 m_nPersonaDataPublicCommendsTeacher; 
    int32 m_nPersonaDataPublicCommendsFriendly; 
    int32 m_nPersonaDataXpTrailLevel; 
    C_UtlVectorEmbeddedNetworkVar< ServerAuthoritativeWeaponSlot_t > m_vecServerAuthoritativeWeaponSlots; 
};

struct  C_IronSightController {
    char m_pad[16];
    char m_pad3_20[3];
    bool m_bIronSightAvailable; 
    float32 m_flIronSightAmount; 
    float32 m_flIronSightAmountGained; 
    float32 m_flIronSightAmountBiased; 
    float32 m_flIronSightAmount_Interpolated; 
    float32 m_flIronSightAmountGained_Interpolated; 
    float32 m_flIronSightAmountBiased_Interpolated; 
    float32 m_flInterpolationLastUpdated; 
    QAngle[8] m_angDeltaAverage; // Size: 96
    QAngle m_angViewLast; // Size: 12
    Vector2D m_vecDotCoords; // Size: 8
    float32 m_flDotBlur; 
    float32 m_flSpeedRatio; 
};

struct __declspec(align(8))  CompositeMaterialMatchFilter_t {
    CompositeMaterialMatchFilterType_t m_nCompositeMaterialMatchFilterType; // Size: 8
    char m_pad[8];
    CUtlString m_strMatchFilter; // Size: 8
    CUtlString m_strMatchValue; // Size: 8
    bool m_bPassWhenTrue; 
};

struct __declspec(align(8))  CompositeMaterialInputLooseVariable_t {
    CUtlString m_strName; // Size: 8
    char m_pad[8];
    char m_pad7_16[7];
    bool m_bExposeExternally; // Size: 8
    CUtlString m_strExposedFriendlyName; // Size: 8
    CUtlString m_strExposedFriendlyGroupName; // Size: 8
    char m_pad7_40[7];
    bool m_bExposedVariableIsFixedRange; // Size: 8
    CUtlString m_strExposedVisibleWhenTrue; // Size: 8
    CUtlString m_strExposedHiddenWhenTrue; // Size: 8
    CompositeMaterialInputLooseVariableType_t m_nVariableType; 
    char m_pad3_64[3];
    bool m_bValueBoolean; 
    int32 m_nValueIntX; 
    int32 m_nValueIntY; 
    int32 m_nValueIntZ; 
    int32 m_nValueIntW; 
    char m_pad3_84[3];
    bool m_bHasFloatBounds; 
    float32 m_flValueFloatX; 
    float32 m_flValueFloatX_Min; 
    float32 m_flValueFloatX_Max; 
    float32 m_flValueFloatY; 
    float32 m_flValueFloatY_Min; 
    float32 m_flValueFloatY_Max; 
    float32 m_flValueFloatZ; 
    float32 m_flValueFloatZ_Min; 
    float32 m_flValueFloatZ_Max; 
    float32 m_flValueFloatW; 
    float32 m_flValueFloatW_Min; 
    float32 m_flValueFloatW_Max; 
    Color m_cValueColor4; 
    CompositeMaterialVarSystemVar_t m_nValueSystemVar; // Size: 8
    CResourceName m_strResourceMaterial; // Size: 224
    CUtlString m_strTextureContentAssetPath; // Size: 8
    CResourceName m_strTextureRuntimeResourcePath; // Size: 224
    CUtlString m_strTextureCompilationVtexTemplate; // Size: 8
    CompositeMaterialInputTextureType_t m_nTextureType; // Size: 8
    CUtlString m_strString; // Size: 8
    CUtlString m_strPanoramaPanelPath; // Size: 8
    int32 m_nPanoramaRenderRes; 
};

struct __declspec(align(8))  CompMatMutatorCondition_t {
    CompMatPropertyMutatorConditionType_t m_nMutatorCondition; // Size: 8
    char m_pad[8];
    CUtlString m_strMutatorConditionContainerName; // Size: 8
    CUtlString m_strMutatorConditionContainerVarName; // Size: 8
    CUtlString m_strMutatorConditionContainerVarValue; // Size: 8
    bool m_bPassWhenTrue; 
};

struct __declspec(align(8))  CompMatPropertyMutator_t {
    char m_pad3_4[3];
    bool m_bEnabled; 
    char m_pad[4];
    CompMatPropertyMutatorType_t m_nMutatorCommandType; 
    CUtlString m_strInitWith_Container; // Size: 8
    CUtlString m_strCopyProperty_InputContainerSrc; // Size: 8
    CUtlString m_strCopyProperty_InputContainerProperty; // Size: 8
    CUtlString m_strCopyProperty_TargetProperty; // Size: 8
    CUtlString m_strRandomRollInputVars_SeedInputVar; // Size: 8
    CUtlVector< CUtlString > m_vecRandomRollInputVars_InputVarsToRoll; // Size: 24
    CUtlString m_strCopyMatchingKeys_InputContainerSrc; // Size: 8
    CUtlString m_strCopyKeysWithSuffix_InputContainerSrc; // Size: 8
    CUtlString m_strCopyKeysWithSuffix_FindSuffix; // Size: 8
    CUtlString m_strCopyKeysWithSuffix_ReplaceSuffix; // Size: 8
    CompositeMaterialInputLooseVariable_t m_nSetValue_Value; // Size: 640
    CUtlString m_strGenerateTexture_TargetParam; // Size: 8
    CUtlString m_strGenerateTexture_InitialContainer; // Size: 8
    int32 m_nResolution; 
    bool m_bIsScratchTarget; 
    bool m_bSplatDebugInfo; 
    char m_pad1_768[1];
    bool m_bCaptureInRenderDoc; 
    CUtlVector< CompMatPropertyMutator_t > m_vecTexGenInstructions; // Size: 24
    CUtlVector< CompMatPropertyMutator_t > m_vecConditionalMutators; // Size: 24
    CUtlString m_strPopInputQueue_Container; // Size: 8
    CUtlString m_strDrawText_InputContainerSrc; // Size: 8
    CUtlString m_strDrawText_InputContainerProperty; // Size: 8
    Vector2D m_vecDrawText_Position; // Size: 8
    Color m_colDrawText_Color; // Size: 8
    CUtlString m_strDrawText_Font; // Size: 8
    CUtlVector< CompMatMutatorCondition_t > m_vecConditions; 
};

struct __declspec(align(8))  CompositeMaterialInputContainer_t {
    char m_pad3_4[3];
    bool m_bEnabled; 
    char m_pad[4];
    CompositeMaterialInputContainerSourceType_t m_nCompositeMaterialInputContainerSourceType; 
    CResourceName m_strSpecificContainerMaterial; // Size: 224
    CUtlString m_strAttrName; // Size: 8
    CUtlString m_strAlias; // Size: 8
    CUtlVector< CompositeMaterialInputLooseVariable_t > m_vecLooseVariables; // Size: 24
    CUtlString m_strAttrNameForVar; // Size: 8
    bool m_bExposeExternally; 
};

struct __declspec(align(8))  CompositeMaterialAssemblyProcedure_t {
    CUtlVector< CResourceName > m_vecCompMatIncludes; // Size: 24
    char m_pad[24];
    CUtlVector< CompositeMaterialMatchFilter_t > m_vecMatchFilters; // Size: 24
    CUtlVector< CompositeMaterialInputContainer_t > m_vecCompositeInputContainers; // Size: 24
    CUtlVector< CompMatPropertyMutator_t > m_vecPropertyMutators; 
};

struct  GeneratedTextureHandle_t {
    CUtlString m_strBitmapName; 
};

struct  CompositeMaterial_t {
    char m_pad[8];
    KeyValues3 m_TargetKVs; // Size: 16
    KeyValues3 m_PreGenerationKVs; // Size: 64
    KeyValues3 m_FinalKVs; // Size: 40
    CUtlVector< GeneratedTextureHandle_t > m_vecGeneratedTextures; 
};

struct __declspec(align(8))  CompositeMaterialEditorPoint_t {
    CResourceName m_ModelName; // Size: 224
    char m_pad[224];
    int32 m_nSequenceIndex; 
    float32 m_flCycle; 
    KeyValues3 m_KVModelStateChoices; // Size: 16
    char m_pad7_256[7];
    bool m_bEnableChildModel; // Size: 8
    CResourceName m_ChildModelName; // Size: 224
    CUtlVector< CompositeMaterialAssemblyProcedure_t > m_vecCompositeMaterialAssemblyProcedures; // Size: 24
    CUtlVector< CompositeMaterial_t > m_vecCompositeMaterials; 
};

struct __declspec(align(8))  CCompositeMaterialEditorDoc {
    char m_pad[8];
    char m_pad4_16[4];
    int32 m_nVersion; // Size: 8
    CUtlVector< CompositeMaterialEditorPoint_t > m_Points; // Size: 24
    KeyValues3 m_KVthumbnail; 
};

struct  CGlobalLightBase {
    char m_pad[16];
    char m_pad3_20[3];
    bool m_bSpotLight; 
    Vector m_SpotLightOrigin; // Size: 12
    QAngle m_SpotLightAngles; // Size: 12
    Vector m_ShadowDirection; // Size: 12
    Vector m_AmbientDirection; // Size: 12
    Vector m_SpecularDirection; // Size: 12
    Vector m_InspectorSpecularDirection; // Size: 12
    float32 m_flSpecularPower; 
    float32 m_flSpecularIndependence; 
    Color m_SpecularColor; 
    bool m_bStartDisabled; 
    bool m_bEnabled; 
    Color m_LightColor; 
    Color m_AmbientColor1; 
    Color m_AmbientColor2; 
    Color m_AmbientColor3; 
    float32 m_flSunDistance; 
    float32 m_flFOV; 
    float32 m_flNearZ; 
    float32 m_flFarZ; 
    bool m_bEnableShadows; 
    bool m_bOldEnableShadows; 
    char m_pad1_144[1];
    bool m_bBackgroundClearNotRequired; 
    float32 m_flCloudScale; 
    float32 m_flCloud1Speed; 
    float32 m_flCloud1Direction; 
    float32 m_flCloud2Speed; 
    char m_pad12_176[12];
    float32 m_flCloud2Direction; // Size: 16
    float32 m_flAmbientScale1; 
    float32 m_flAmbientScale2; 
    float32 m_flGroundScale; 
    float32 m_flLightScale; 
    float32 m_flFoWDarkness; 
    char m_pad3_200[3];
    bool m_bEnableSeparateSkyboxFog; 
    Vector m_vFowColor; // Size: 12
    Vector m_ViewOrigin; // Size: 12
    QAngle m_ViewAngles; // Size: 12
    float32 m_flViewFoV; 
    Vector[8] m_WorldPoints; // Size: 952
    Vector2D m_vFogOffsetLayer0; // Size: 8
    Vector2D m_vFogOffsetLayer1; // Size: 8
    CHandle< C_BaseEntity > m_hEnvWind; 
    CHandle< C_BaseEntity > m_hEnvSky; 
};

struct __declspec(align(16))  C_GlobalLight {
    char m_pad[2608];
    uint16 m_WindClothForceHandle; 
};

struct  C_CSGO_PreviewModel_GraphController {
    char m_pad[96];
    CAnimGraphParamOptionalRef< char* > m_pszCharacterMode; // Size: 40
    CAnimGraphParamOptionalRef< char* > m_pszWeaponState; // Size: 40
    CAnimGraphParamOptionalRef< char* > m_pszWeaponType; // Size: 40
    CAnimGraphParamOptionalRef< char* > m_pszEndOfMatchCelebration; 
};

struct  C_CSGO_PreviewPlayer_GraphController {
    char m_pad[96];
    CAnimGraphParamOptionalRef< char* > m_pszCharacterMode; // Size: 40
    CAnimGraphParamOptionalRef< char* > m_pszTeamPreviewVariant; // Size: 40
    CAnimGraphParamOptionalRef< char* > m_pszTeamPreviewPosition; // Size: 40
    CAnimGraphParamOptionalRef< char* > m_pszEndOfMatchCelebration; // Size: 40
    CAnimGraphParamOptionalRef< int32 > m_nTeamPreviewRandom; // Size: 32
    CAnimGraphParamOptionalRef< char* > m_pszWeaponState; // Size: 40
    CAnimGraphParamOptionalRef< char* > m_pszWeaponType; // Size: 40
    CAnimGraphParamOptionalRef< bool > m_bCT; 
};

struct __declspec(align(8))  C_CSGO_MapPreviewCameraPathNode {
    char m_pad[1384];
    CUtlSymbolLarge m_szParentPathUniqueID; // Size: 8
    int32 m_nPathIndex; 
    Vector m_vInTangentLocal; // Size: 12
    Vector m_vOutTangentLocal; // Size: 12
    float32 m_flFOV; 
    float32 m_flCameraSpeed; 
    float32 m_flEaseIn; 
    float32 m_flEaseOut; 
    Vector m_vInTangentWorld; // Size: 12
    Vector m_vOutTangentWorld; 
};

struct __declspec(align(8))  C_CSGO_MapPreviewCameraPath {
    char m_pad[1384];
    float32 m_flZFar; 
    float32 m_flZNear; 
    bool m_bLoop; 
    bool m_bVerticalFOV; 
    char m_pad1_1396[1];
    bool m_bConstantSpeed; 
    char m_pad64_1464[64];
    float32 m_flDuration; // Size: 68
    float32 m_flPathLength; 
    float32 m_flPathDuration; 
};

struct  CCSPlayer_GlowServices {
};

struct __declspec(align(8))  C_VoteController {
    char m_pad[1400];
    int32 m_iActiveIssueIndex; 
    int32 m_iOnlyTeamToVote; 
    int32[5] m_nVoteOptionCount; // Size: 20
    int32 m_nPotentialVotes; 
    bool m_bVotesDirty; 
    bool m_bTypeDirty; 
    bool m_bIsYesNoVote; 
};

struct __declspec(align(8))  C_MapVetoPickController {
    char m_pad[1400];
    int32 m_nDraftType; 
    int32 m_nTeamWinningCoinToss; 
    int32[64] m_nTeamWithFirstChoice; // Size: 256
    int32[7] m_nVoteMapIdsList; // Size: 28
    int32[64] m_nAccountIDs; // Size: 256
    int32[64] m_nMapId0; // Size: 256
    int32[64] m_nMapId1; // Size: 256
    int32[64] m_nMapId2; // Size: 256
    int32[64] m_nMapId3; // Size: 256
    int32[64] m_nMapId4; // Size: 256
    int32[64] m_nMapId5; // Size: 256
    int32[64] m_nStartingSide0; // Size: 256
    int32 m_nCurrentPhase; 
    int32 m_nPhaseStartTick; 
    int32 m_nPhaseDurationTicks; 
    int32 m_nPostDataUpdateTick; 
    bool m_bDisabledHud; 
};

struct  CPlayerSprayDecalRenderHelper {
};

struct  C_CSGO_TeamPreviewCamera {
    char m_pad[1488];
    int32 m_nVariant; 
    char m_pad3_1496[3];
    bool m_bDofEnabled; 
    float32 m_flDofNearBlurry; 
    float32 m_flDofNearCrisp; 
    float32 m_flDofFarCrisp; 
    float32 m_flDofFarBlurry; 
    float32 m_flDofTiltToGround; 
};

struct __declspec(align(8))  C_CSGO_TeamSelectCamera {
};

struct __declspec(align(8))  C_CSGO_TerroristTeamIntroCamera {
};

struct __declspec(align(8))  C_CSGO_TerroristWingmanIntroCamera {
};

struct __declspec(align(8))  C_CSGO_CounterTerroristTeamIntroCamera {
};

struct __declspec(align(8))  C_CSGO_CounterTerroristWingmanIntroCamera {
};

struct __declspec(align(8))  C_CSGO_EndOfMatchCamera {
};

struct __declspec(align(8))  C_CSGO_EndOfMatchCharacterPosition {
};

struct  C_CSGO_EndOfMatchLineupEndpoint {
};

struct __declspec(align(8))  C_CSGO_EndOfMatchLineupStart {
};

struct __declspec(align(8))  C_CSGO_EndOfMatchLineupEnd {
};

struct __declspec(align(8))  C_CsmFovOverride {
    char m_pad[1384];
    CUtlString m_cameraName; // Size: 8
    float32 m_flCsmFovOverrideValue; 
};

struct  C_Chicken_GraphController {
    char m_pad[96];
    CAnimGraphParamRef< char* > m_paramActivity; // Size: 40
    CAnimGraphParamRef< bool > m_paramEndActivityImmediately; // Size: 32
    CAnimGraphParamRef< bool > m_paramSnapToSquatting; // Size: 32
    CAnimGraphTagRef m_sActivityFinished; // Size: 24
    float32 m_flSquatProbability; 
};

struct __declspec(align(8))  C_PointEntity {
};

struct __declspec(align(8))  C_EnvCombinedLightProbeVolume {
    char m_pad[5576];
    Color m_Entity_Color; 
    float32 m_Entity_flBrightness; 
    CStrongHandle< InfoForResourceTypeCTextureBase > m_Entity_hCubemapTexture; // Size: 8
    char m_pad7_5600[7];
    bool m_Entity_bCustomCubemapTexture; // Size: 8
    CStrongHandle< InfoForResourceTypeCTextureBase > m_Entity_hLightProbeTexture; // Size: 8
    CStrongHandle< InfoForResourceTypeCTextureBase > m_Entity_hLightProbeDirectLightIndicesTexture; // Size: 8
    CStrongHandle< InfoForResourceTypeCTextureBase > m_Entity_hLightProbeDirectLightScalarsTexture; // Size: 8
    CStrongHandle< InfoForResourceTypeCTextureBase > m_Entity_hLightProbeDirectLightShadowsTexture; // Size: 8
    Vector m_Entity_vBoxMins; // Size: 12
    Vector m_Entity_vBoxMaxs; // Size: 12
    char m_pad3_5660[3];
    bool m_Entity_bMoveable; 
    int32 m_Entity_nHandshake; 
    int32 m_Entity_nEnvCubeMapArrayIndex; 
    int32 m_Entity_nPriority; 
    char m_pad3_5676[3];
    bool m_Entity_bStartDisabled; 
    float32 m_Entity_flEdgeFadeDist; 
    Vector m_Entity_vEdgeFadeDists; // Size: 12
    int32 m_Entity_nLightProbeSizeX; 
    int32 m_Entity_nLightProbeSizeY; 
    int32 m_Entity_nLightProbeSizeZ; 
    int32 m_Entity_nLightProbeAtlasX; 
    int32 m_Entity_nLightProbeAtlasY; 
    char m_pad21_5737[21];
    int32 m_Entity_nLightProbeAtlasZ; // Size: 25
    bool m_Entity_bEnabled; 
};

struct __declspec(align(8))  C_EnvCubemap {
    char m_pad[1512];
    CStrongHandle< InfoForResourceTypeCTextureBase > m_Entity_hCubemapTexture; // Size: 8
    char m_pad3_1524[3];
    bool m_Entity_bCustomCubemapTexture; 
    float32 m_Entity_flInfluenceRadius; 
    Vector m_Entity_vBoxProjectMins; // Size: 12
    Vector m_Entity_vBoxProjectMaxs; // Size: 12
    char m_pad3_1556[3];
    bool m_Entity_bMoveable; 
    int32 m_Entity_nHandshake; 
    int32 m_Entity_nEnvCubeMapArrayIndex; 
    int32 m_Entity_nPriority; 
    float32 m_Entity_flEdgeFadeDist; 
    Vector m_Entity_vEdgeFadeDists; // Size: 12
    float32 m_Entity_flDiffuseScale; 
    bool m_Entity_bStartDisabled; 
    bool m_Entity_bDefaultEnvMap; 
    bool m_Entity_bDefaultSpecEnvMap; 
    bool m_Entity_bIndoorCubeMap; 
    char m_pad15_1608[15];
    bool m_Entity_bCopyDiffuseFromDefaultCubemap; // Size: 16
    bool m_Entity_bEnabled; 
};

struct __declspec(align(8))  C_EnvCubemapBox {
};

struct __declspec(align(8))  C_EnvCubemapFog {
    char m_pad[1384];
    float32 m_flEndDistance; 
    float32 m_flStartDistance; 
    float32 m_flFogFalloffExponent; 
    char m_pad3_1400[3];
    bool m_bHeightFogEnabled; 
    float32 m_flFogHeightWidth; 
    float32 m_flFogHeightEnd; 
    float32 m_flFogHeightStart; 
    float32 m_flFogHeightExponent; 
    float32 m_flLODBias; 
    bool m_bActive; 
    char m_pad2_1424[2];
    bool m_bStartDisabled; 
    float32 m_flFogMaxOpacity; 
    int32 m_nCubemapSourceType; 
    CStrongHandle< InfoForResourceTypeIMaterial2 > m_hSkyMaterial; // Size: 8
    CUtlSymbolLarge m_iszSkyEntity; // Size: 8
    CStrongHandle< InfoForResourceTypeCTextureBase > m_hFogCubemapTexture; // Size: 8
    bool m_bHasHeightFogEnd; 
    bool m_bFirstTime; 
};

struct __declspec(align(8))  C_GradientFog {
    char m_pad[1384];
    CStrongHandle< InfoForResourceTypeCTextureBase > m_hGradientFogTexture; // Size: 8
    float32 m_flFogStartDistance; 
    float32 m_flFogEndDistance; 
    char m_pad3_1404[3];
    bool m_bHeightFogEnabled; 
    float32 m_flFogStartHeight; 
    float32 m_flFogEndHeight; 
    float32 m_flFarZ; 
    float32 m_flFogMaxOpacity; 
    float32 m_flFogFalloffExponent; 
    float32 m_flFogVerticalExponent; 
    Color m_fogColor; 
    float32 m_flFogStrength; 
    float32 m_flFadeTime; 
    bool m_bStartDisabled; 
    bool m_bIsEnabled; 
    bool m_bGradientFogNeedsTextures; 
};

struct __declspec(align(8))  C_EnvLightProbeVolume {
    char m_pad[5448];
    CStrongHandle< InfoForResourceTypeCTextureBase > m_Entity_hLightProbeTexture; // Size: 8
    CStrongHandle< InfoForResourceTypeCTextureBase > m_Entity_hLightProbeDirectLightIndicesTexture; // Size: 8
    CStrongHandle< InfoForResourceTypeCTextureBase > m_Entity_hLightProbeDirectLightScalarsTexture; // Size: 8
    CStrongHandle< InfoForResourceTypeCTextureBase > m_Entity_hLightProbeDirectLightShadowsTexture; // Size: 8
    Vector m_Entity_vBoxMins; // Size: 12
    Vector m_Entity_vBoxMaxs; // Size: 12
    char m_pad3_5508[3];
    bool m_Entity_bMoveable; 
    int32 m_Entity_nHandshake; 
    int32 m_Entity_nPriority; 
    char m_pad3_5520[3];
    bool m_Entity_bStartDisabled; 
    int32 m_Entity_nLightProbeSizeX; 
    int32 m_Entity_nLightProbeSizeY; 
    int32 m_Entity_nLightProbeSizeZ; 
    int32 m_Entity_nLightProbeAtlasX; 
    int32 m_Entity_nLightProbeAtlasY; 
    char m_pad9_5553[9];
    int32 m_Entity_nLightProbeAtlasZ; // Size: 13
    bool m_Entity_bEnabled; 
};

struct __declspec(align(8))  C_PlayerVisibility {
    char m_pad[1384];
    float32 m_flVisibilityStrength; 
    float32 m_flFogDistanceMultiplier; 
    float32 m_flFogMaxDensityMultiplier; 
    float32 m_flFadeTime; 
    bool m_bStartDisabled; 
    bool m_bIsEnabled; 
};

struct __declspec(align(8))  C_EnvVolumetricFogController {
    char m_pad[1384];
    float32 m_flScattering; 
    float32 m_flAnisotropy; 
    float32 m_flFadeSpeed; 
    float32 m_flDrawDistance; 
    float32 m_flFadeInStart; 
    float32 m_flFadeInEnd; 
    float32 m_flIndirectStrength; 
    int32 m_nVolumeDepth; 
    float32 m_fFirstVolumeSliceThickness; 
    int32 m_nIndirectTextureDimX; 
    int32 m_nIndirectTextureDimY; 
    int32 m_nIndirectTextureDimZ; 
    Vector m_vBoxMins; // Size: 12
    Vector m_vBoxMaxs; // Size: 12
    char m_pad3_1460[3];
    bool m_bActive; 
    GameTime_t m_flStartAnisoTime; 
    GameTime_t m_flStartScatterTime; 
    GameTime_t m_flStartDrawDistanceTime; 
    float32 m_flStartAnisotropy; 
    float32 m_flStartScattering; 
    float32 m_flStartDrawDistance; 
    float32 m_flDefaultAnisotropy; 
    float32 m_flDefaultScattering; 
    float32 m_flDefaultDrawDistance; 
    bool m_bStartDisabled; 
    bool m_bEnableIndirect; 
    bool m_bIndirectUseLPVs; 
    char m_pad4_1504[4];
    bool m_bIsMaster; 
    CStrongHandle< InfoForResourceTypeCTextureBase > m_hFogIndirectTexture; // Size: 8
    int32 m_nForceRefreshCount; 
    float32 m_fNoiseSpeed; 
    float32 m_fNoiseStrength; 
    Vector m_vNoiseScale; // Size: 12
    bool m_bFirstTime; 
};

struct __declspec(align(8))  C_EnvVolumetricFogVolume {
    char m_pad[1384];
    char m_pad3_1388[3];
    bool m_bActive; 
    Vector m_vBoxMins; // Size: 12
    Vector m_vBoxMaxs; // Size: 12
    char m_pad3_1416[3];
    bool m_bStartDisabled; 
    float32 m_flStrength; 
    int32 m_nFalloffShape; 
    float32 m_flFalloffExponent; 
    float32 m_flHeightFogDepth; 
    float32 m_fHeightFogEdgeWidth; 
    float32 m_fIndirectLightStrength; 
    float32 m_fSunLightStrength; 
    float32 m_fNoiseStrength; 
    bool m_bOverrideIndirectLightStrength; 
    bool m_bOverrideSunLightStrength; 
    bool m_bOverrideNoiseStrength; 
    bool m_bAllowLPVIndirect; 
};

struct __declspec(align(8))  CInfoTarget {
};

struct __declspec(align(8))  CInfoParticleTarget {
};

struct __declspec(align(8))  C_InfoVisibilityBox {
    char m_pad[1388];
    int32 m_nMode; 
    Vector m_vBoxSize; // Size: 12
    bool m_bEnabled; 
};

struct __declspec(align(8))  CInfoWorldLayer {
    char m_pad[1384];
    CEntityIOOutput m_pOutputOnEntitiesSpawned; // Size: 40
    CUtlSymbolLarge m_worldName; // Size: 8
    CUtlSymbolLarge m_layerName; // Size: 8
    bool m_bWorldLayerVisible; 
    bool m_bEntitiesSpawned; 
    char m_pad1_1444[1];
    bool m_bCreateAsChildSpawnGroup; 
    uint32 m_hLayerSpawnGroup; 
    bool m_bWorldLayerActuallyVisible; 
};

struct __declspec(align(8))  CPointChildModifier {
    char m_pad[1384];
    bool m_bOrphanInsteadOfDeletingChildrenOnRemove; 
};

struct __declspec(align(8))  C_PointCameraVFOV {
    char m_pad[1480];
    float32 m_flVerticalFOV; 
};

struct __declspec(align(8))  CPointTemplate {
    char m_pad[1384];
    CUtlSymbolLarge m_iszWorldName; // Size: 8
    CUtlSymbolLarge m_iszSource2EntityLumpName; // Size: 8
    CUtlSymbolLarge m_iszEntityFilterName; // Size: 8
    float32 m_flTimeoutInterval; 
    char m_pad3_1416[3];
    bool m_bAsynchronouslySpawnEntities; 
    CEntityIOOutput m_pOutputOnSpawned; // Size: 40
    PointTemplateClientOnlyEntityBehavior_t m_clientOnlyEntityBehavior; 
    PointTemplateOwnerSpawnGroupType_t m_ownerSpawnGroupType; 
    CUtlVector< uint32 > m_createdSpawnGroupHandles; // Size: 24
    CUtlVector< CEntityHandle > m_SpawnedEntityHandles; // Size: 24
    HSCRIPT m_ScriptSpawnCallback; // Size: 8
    HSCRIPT m_ScriptCallbackScope; 
};

struct __declspec(align(8))  CRagdollManager {
    char m_pad[1384];
    int8 m_iCurrentMaxRagdollCount; 
};

struct  C_SoundAreaEntityBase {
    char m_pad[1384];
    char m_pad7_1392[7];
    bool m_bDisabled; // Size: 8
    char m_pad7_1400[7];
    bool m_bWasEnabled; // Size: 8
    CUtlSymbolLarge m_iszSoundAreaType; // Size: 8
    Vector m_vPos; 
};

struct __declspec(align(8))  C_SoundAreaEntitySphere {
    char m_pad[1424];
    float32 m_flRadius; 
};

struct __declspec(align(8))  C_SoundAreaEntityOrientedBox {
    char m_pad[1424];
    Vector m_vMin; // Size: 12
    Vector m_vMax; 
};

struct __declspec(align(8))  C_SoundEventEntity {
    char m_pad[1384];
    bool m_bStartOnSpawn; 
    bool m_bToLocalPlayer; 
    bool m_bStopOnNew; 
    bool m_bSaveRestore; 
    char m_pad3_1392[3];
    bool m_bSavedIsPlaying; 
    char m_pad4_1400[4];
    float32 m_flSavedElapsedTime; // Size: 8
    CUtlSymbolLarge m_iszSourceEntityName; // Size: 8
    CUtlSymbolLarge m_iszAttachmentName; // Size: 8
    CEntityOutputTemplate< uint64 > m_onGUIDChanged; // Size: 40
    CEntityIOOutput m_onSoundFinished; // Size: 40
    char m_pad44_1544[44];
    float32 m_flClientCullRadius; // Size: 48
    CUtlSymbolLarge m_iszSoundName; // Size: 16
    CEntityHandle m_hSource; 
    int32 m_nEntityIndexSelection; 
    bitfield:1 m_bClientSideOnly; 
};

struct __declspec(align(8))  C_SoundEventEntityAlias_snd_event_point {
};

struct __declspec(align(8))  C_SoundEventAABBEntity {
    char m_pad[1576];
    Vector m_vMins; // Size: 12
    Vector m_vMaxs; 
};

struct __declspec(align(8))  C_SoundEventOBBEntity {
    char m_pad[1576];
    Vector m_vMins; // Size: 12
    Vector m_vMaxs; 
};

struct __declspec(align(8))  C_SoundEventSphereEntity {
    char m_pad[1576];
    float32 m_flRadius; 
};

struct __declspec(align(8))  C_SoundEventPathCornerEntity {
    char m_pad[1576];
    C_NetworkUtlVectorBase< SoundeventPathCornerPairNetworked_t > m_vecCornerPairsNetworked; 
};

struct __declspec(align(8))  C_BasePlayerPawn {
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
    C_UtlVectorEmbeddedNetworkVar< ViewAngleServerChange_t > m_ServerViewAngleChanges; // Size: 80
    uint32 m_nHighestConsumedServerViewAngleChangeIndex; 
    QAngle v_angle; // Size: 12
    QAngle v_anglePrevious; // Size: 12
    uint32 m_iHideHUD; 
    sky3dparams_t m_skybox3d; // Size: 144
    GameTime_t m_flDeathTime; 
    Vector m_vecPredictionError; // Size: 12
    GameTime_t m_flPredictionErrorTime; 
    Vector m_vecLastCameraSetupLocalOrigin; // Size: 12
    GameTime_t m_flLastCameraSetupTime; 
    float32 m_flFOVSensitivityAdjust; 
    float32 m_flMouseSensitivity; 
    Vector m_vOldOrigin; // Size: 12
    float32 m_flOldSimulationTime; 
    int32 m_nLastExecutedCommandNumber; 
    int32 m_nLastExecutedCommandTick; 
    CHandle< CBasePlayerController > m_hController; 
    bool m_bIsSwappingToPredictableController; 
};

struct __declspec(align(8))  C_Team {
    char m_pad[1384];
    C_NetworkUtlVectorBase< CHandle< CBasePlayerController > > m_aPlayerControllers; // Size: 24
    C_NetworkUtlVectorBase< CHandle< C_BasePlayerPawn > > m_aPlayers; // Size: 24
    int32 m_iScore; 
    char[129] m_szTeamname; 
};

struct __declspec(align(8))  CBasePlayerVData {
    char m_pad[40];
    CResourceNameTyped< CWeakHandle< InfoForResourceTypeCModel > > m_sModelName; // Size: 224
    CSkillFloat m_flHeadDamageMultiplier; // Size: 16
    CSkillFloat m_flChestDamageMultiplier; // Size: 16
    CSkillFloat m_flStomachDamageMultiplier; // Size: 16
    CSkillFloat m_flArmDamageMultiplier; // Size: 16
    CSkillFloat m_flLegDamageMultiplier; // Size: 16
    float32 m_flHoldBreathTime; 
    float32 m_flDrowningDamageInterval; 
    int32 m_nDrowningDamageInitial; 
    int32 m_nDrowningDamageMax; 
    int32 m_nWaterSpeed; 
    float32 m_flUseRange; 
    float32 m_flUseAngleTolerance; 
    float32 m_flCrouchTime; 
};

struct __declspec(align(8))  CBasePlayerWeaponVData {
    char m_pad[40];
    CResourceNameTyped< CWeakHandle< InfoForResourceTypeCModel > > m_szWorldModel; // Size: 224
    CResourceNameTyped< CWeakHandle< InfoForResourceTypeCModel > > m_sToolsOnlyOwnerModelName; // Size: 224
    bool m_bBuiltRightHanded; 
    char m_pad6_496[6];
    bool m_bAllowFlipping; 
    CAttachmentNameSymbolWithStorage m_sMuzzleAttachment; // Size: 32
    CResourceNameTyped< CWeakHandle< InfoForResourceTypeIParticleSystemDefinition > > m_szMuzzleFlashParticle; // Size: 224
    bool m_bLinkedCooldowns; 
    ItemFlagTypes_t m_iFlags; 
    AmmoIndex_t m_nPrimaryAmmoType; 
    AmmoIndex_t m_nSecondaryAmmoType; 
    int32 m_iMaxClip1; 
    int32 m_iMaxClip2; 
    int32 m_iDefaultClip1; 
    int32 m_iDefaultClip2; 
    char m_pad3_776[3];
    bool m_bReserveAmmoAsClips; 
    int32 m_iWeight; 
    bool m_bAutoSwitchTo; 
    char m_pad2_784[2];
    bool m_bAutoSwitchFrom; 
    RumbleEffect_t m_iRumbleEffect; 
    int32 m_iSlot; 
    char m_pad4_800[4];
    int32 m_iPosition; // Size: 8
    CUtlOrderedMap< WeaponSound_t, CSoundEventName > m_aShootSounds; 
};

struct  CClientAlphaProperty {
    char m_pad[16];
    uint8 m_nRenderFX; 
    uint8 m_nRenderMode; 
    bitfield:1 m_bAlphaOverride; 
    bitfield:1 m_bShadowAlphaOverride; 
    bitfield:6 m_nReserved; // Size: 19
    uint8 m_nAlpha; 
    uint16 m_nDesyncOffset; 
    uint16 m_nReserved2; 
    uint16 m_nDistFadeStart; 
    uint16 m_nDistFadeEnd; 
    float32 m_flFadeScale; 
    GameTime_t m_flRenderFxStartTime; 
    float32 m_flRenderFxDuration; 
};

struct __declspec(align(8))  CServerOnlyModelEntity {
};

struct __declspec(align(8))  C_ModelPointEntity {
};

struct __declspec(align(8))  CLogicRelay {
    char m_pad[1384];
    CEntityIOOutput m_OnTrigger; // Size: 40
    CEntityIOOutput m_OnSpawn; // Size: 40
    bool m_bDisabled; 
    bool m_bWaitForRefire; 
    bool m_bTriggerOnce; 
    bool m_bFastRetrigger; 
    bool m_bPassthoughCaller; 
};

struct __declspec(align(8))  C_ParticleSystem {
    char m_pad[3368];
    char[512] m_szSnapshotFileName; // Size: 512
    bool m_bActive; 
    char m_pad2_3884[2];
    bool m_bFrozen; 
    float32 m_flFreezeTransitionDuration; 
    int32 m_nStopType; 
    char m_pad3_3896[3];
    bool m_bAnimateDuringGameplayPause; 
    CStrongHandle< InfoForResourceTypeIParticleSystemDefinition > m_iEffectIndex; // Size: 8
    GameTime_t m_flStartTime; 
    float32 m_flPreSimTime; 
    Vector[4] m_vServerControlPoints; // Size: 48
    uint8[4] m_iServerControlPointAssignments; 
    CHandle< C_BaseEntity >[64] m_hControlPointEnts; // Size: 256
    bool m_bNoSave; 
    bool m_bNoFreeze; 
    bool m_bNoRamp; 
    bool m_bStartActive; 
    CUtlSymbolLarge m_iszEffectName; // Size: 8
    CUtlSymbolLarge[64] m_iszControlPointNames; // Size: 512
    int32 m_nDataCP; 
    Vector m_vecDataCPValue; // Size: 12
    int32 m_nTintCP; 
    Color m_clrTint; // Size: 36
    bool m_bOldActive; 
    bool m_bOldFrozen; 
};

struct __declspec(align(8))  C_PathParticleRope {
    char m_pad[1392];
    char m_pad3_1396[3];
    bool m_bStartActive; 
    float32 m_flMaxSimulationTime; 
    CUtlSymbolLarge m_iszEffectName; // Size: 8
    CUtlVector< CUtlSymbolLarge > m_PathNodes_Name; // Size: 24
    float32 m_flParticleSpacing; 
    float32 m_flSlack; 
    float32 m_flRadius; 
    Color m_ColorTint; 
    char m_pad4_1456[4];
    int32 m_nEffectState; // Size: 8
    CStrongHandle< InfoForResourceTypeIParticleSystemDefinition > m_iEffectIndex; // Size: 8
    C_NetworkUtlVectorBase< Vector > m_PathNodes_Position; // Size: 24
    C_NetworkUtlVectorBase< Vector > m_PathNodes_TangentIn; // Size: 24
    C_NetworkUtlVectorBase< Vector > m_PathNodes_TangentOut; // Size: 24
    C_NetworkUtlVectorBase< Vector > m_PathNodes_Color; // Size: 24
    C_NetworkUtlVectorBase< bool > m_PathNodes_PinEnabled; // Size: 24
    C_NetworkUtlVectorBase< float32 > m_PathNodes_RadiusScale; 
};

struct __declspec(align(8))  C_PathParticleRopeAlias_path_particle_rope_clientside {
};

struct __declspec(align(8))  CPathSimple {
    char m_pad[1472];
    CUtlString m_pathString; 
};

struct __declspec(align(8))  C_DynamicLight {
    char m_pad[3368];
    uint8 m_Flags; 
    char m_pad2_3372[2];
    uint8 m_LightStyle; 
    float32 m_Radius; 
    int32 m_Exponent; 
    float32 m_InnerAngle; 
    float32 m_OuterAngle; 
    float32 m_SpotRadius; 
};

struct __declspec(align(8))  C_EnvScreenOverlay {
    char m_pad[1384];
    CUtlSymbolLarge[10] m_iszOverlayNames; // Size: 80
    float32[10] m_flOverlayTimes; // Size: 40
    GameTime_t m_flStartTime; 
    int32 m_iDesiredOverlay; 
    bool m_bIsActive; 
    char m_pad2_1516[2];
    bool m_bWasActive; 
    int32 m_iCachedDesiredOverlay; 
    int32 m_iCurrentOverlay; 
    GameTime_t m_flCurrentOverlayTime; 
};

struct __declspec(align(8))  C_FuncTrackTrain {
    char m_pad[3368];
    int32 m_nLongAxis; 
    float32 m_flRadius; 
    float32 m_flLineLength; 
};

struct  C_LightGlowOverlay {
    char m_pad[208];
    Vector m_vecOrigin; // Size: 12
    Vector m_vecDirection; // Size: 12
    int32 m_nMinDist; 
    int32 m_nMaxDist; 
    int32 m_nOuterMaxDist; 
    bool m_bOneSided; 
    bool m_bModulateByDot; 
};

struct __declspec(align(8))  C_LightGlow {
    char m_pad[3368];
    uint32 m_nHorizontalSize; 
    uint32 m_nVerticalSize; 
    uint32 m_nMinDist; 
    uint32 m_nMaxDist; 
    uint32 m_nOuterMaxDist; 
    float32 m_flGlowProxySize; 
    char m_pad4_3400[4];
    float32 m_flHDRColorScale; // Size: 8
    C_LightGlowOverlay m_GlowOverlay; 
};

struct __declspec(align(8))  C_SpotlightEnd {
    char m_pad[3368];
    float32 m_flLightScale; 
    float32 m_Radius; 
};

struct __declspec(align(8))  C_PointValueRemapper {
    char m_pad[1384];
    bool m_bDisabled; 
    bool m_bDisabledOld; 
    char m_pad1_1388[1];
    bool m_bUpdateOnClient; 
    ValueRemapperInputType_t m_nInputType; 
    CHandle< C_BaseEntity > m_hRemapLineStart; 
    CHandle< C_BaseEntity > m_hRemapLineEnd; 
    float32 m_flMaximumChangePerSecond; 
    float32 m_flDisengageDistance; 
    float32 m_flEngageDistance; 
    char m_pad3_1416[3];
    bool m_bRequiresUseKey; 
    ValueRemapperOutputType_t m_nOutputType; // Size: 8
    C_NetworkUtlVectorBase< CHandle< C_BaseEntity > > m_hOutputEntities; // Size: 24
    ValueRemapperHapticsType_t m_nHapticsType; 
    ValueRemapperMomentumType_t m_nMomentumType; 
    float32 m_flMomentumModifier; 
    float32 m_flSnapValue; 
    float32 m_flCurrentMomentum; 
    ValueRemapperRatchetType_t m_nRatchetType; 
    float32 m_flRatchetOffset; 
    float32 m_flInputOffset; 
    bool m_bEngaged; 
    char m_pad2_1484[2];
    bool m_bFirstUpdate; 
    float32 m_flPreviousValue; 
    GameTime_t m_flPreviousUpdateTickTime; 
    Vector m_vecPreviousTestPoint; 
};

struct __declspec(align(8))  C_PointWorldText {
    char m_pad[3376];
    char m_pad15_3392[15];
    bool m_bForceRecreateNextUpdate; // Size: 16
    char[512] m_messageText; // Size: 512
    char[64] m_FontName; // Size: 64
    bool m_bEnabled; 
    char m_pad2_3972[2];
    bool m_bFullbright; 
    float32 m_flWorldUnitsPerPx; 
    float32 m_flFontSize; 
    float32 m_flDepthOffset; 
    Color m_Color; 
    PointWorldTextJustifyHorizontal_t m_nJustifyHorizontal; 
    PointWorldTextJustifyVertical_t m_nJustifyVertical; 
    PointWorldTextReorientMode_t m_nReorientMode; 
};

struct __declspec(align(8))  CCitadelSoundOpvarSetOBB {
    char m_pad[1408];
    CUtlSymbolLarge m_iszStackName; // Size: 8
    CUtlSymbolLarge m_iszOperatorName; // Size: 8
    CUtlSymbolLarge m_iszOpvarName; // Size: 8
    Vector m_vDistanceInnerMins; // Size: 12
    Vector m_vDistanceInnerMaxs; // Size: 12
    Vector m_vDistanceOuterMins; // Size: 12
    Vector m_vDistanceOuterMaxs; // Size: 12
    int32 m_nAABBDirection; 
};

struct __declspec(align(8))  C_HandleTest {
    char m_pad[1384];
    CHandle< C_BaseEntity > m_Handle; 
    bool m_bSendHandle; 
};

struct __declspec(align(8))  C_EnvWind {
    char m_pad[1384];
    C_EnvWindShared m_EnvWindShared; 
};

struct __declspec(align(8))  C_BaseToggle {
};

struct __declspec(align(8))  C_BaseButton {
    char m_pad[3368];
    CHandle< C_BaseModelEntity > m_glowEntity; 
    char m_pad3_3376[3];
    bool m_usable; 
    CUtlSymbolLarge m_szDisplayText; 
};

struct __declspec(align(8))  C_PrecipitationBlocker {
};

struct __declspec(align(8))  C_EntityDissolve {
    char m_pad[3376];
    GameTime_t m_flStartTime; 
    float32 m_flFadeInStart; 
    float32 m_flFadeInLength; 
    float32 m_flFadeOutModelStart; 
    float32 m_flFadeOutModelLength; 
    float32 m_flFadeOutStart; 
    float32 m_flFadeOutLength; 
    GameTime_t m_flNextSparkTime; 
    EntityDisolveType_t m_nDissolveType; 
    Vector m_vDissolverOrigin; // Size: 12
    uint32 m_nMagnitude; 
    bool m_bCoreExplode; 
    bool m_bLinkedToServerEnt; 
};

struct __declspec(align(8))  C_EnvProjectedTexture {
};

struct __declspec(align(8))  C_EnvDecal {
    char m_pad[3368];
    CStrongHandle< InfoForResourceTypeIMaterial2 > m_hDecalMaterial; // Size: 8
    float32 m_flWidth; 
    float32 m_flHeight; 
    float32 m_flDepth; 
    uint32 m_nRenderOrder; 
    bool m_bProjectOnWorld; 
    bool m_bProjectOnCharacters; 
    char m_pad1_3396[1];
    bool m_bProjectOnWater; 
    float32 m_flDepthSortBias; 
};

struct __declspec(align(8))  C_FuncBrush {
};

struct __declspec(align(8))  C_FuncElectrifiedVolume {
    char m_pad[3368];
    ParticleIndex_t m_nAmbientEffect; // Size: 8
    CUtlSymbolLarge m_EffectName; // Size: 8
    bool m_bState; 
};

struct __declspec(align(8))  C_FuncRotating {
};

struct __declspec(align(8))  C_Breakable {
};

struct __declspec(align(8))  C_PhysBox {
};

struct __declspec(align(8))  C_BaseFlex {
    char m_pad[3992];
    C_NetworkUtlVectorBase< float32 > m_flexWeight; // Size: 24
    Vector m_vLookTargetPosition; // Size: 24
    char m_pad95_4136[95];
    bool m_blinktoggle; // Size: 96
    int32 m_nLastFlexUpdateFrameCount; 
    Vector m_CachedViewTarget; // Size: 12
    SceneEventId_t m_nNextSceneEventId; 
    int32 m_iBlink; 
    float32 m_blinktime; 
    char m_pad3_4168[3];
    bool m_prevblinktoggle; 
    int32 m_iJawOpen; 
    float32 m_flJawOpenAmount; 
    float32 m_flBlinkAmount; 
    AttachmentHandle_t m_iMouthAttachment; 
    AttachmentHandle_t m_iEyeAttachment; 
    char m_pad25_4208[25];
    bool m_bResetFlexWeightsOnModelChange; // Size: 26
    int32 m_nEyeOcclusionRendererBone; 
    matrix3x4_t m_mEyeOcclusionRendererCameraToBoneTransform; // Size: 48
    Vector m_vEyeOcclusionRendererHalfExtent; // Size: 28
    C_BaseFlex::Emphasized_Phoneme[3] m_PhonemeClasses; 
};

struct __declspec(align(8))  C_SceneEntity {
    char m_pad[1392];
    bool m_bIsPlayingBack; 
    bool m_bPaused; 
    bool m_bMultiplayer; 
    bool m_bAutogenerated; 
    float32 m_flForceClientTime; 
    uint16 m_nSceneStringIndex; 
    char m_pad1_1404[1];
    bool m_bClientOnly; 
    CHandle< C_BaseFlex > m_hOwner; 
    C_NetworkUtlVectorBase< CHandle< C_BaseFlex > > m_hActorList; // Size: 24
    char m_pad15_1448[15];
    bool m_bWasPlaying; // Size: 16
    CUtlVector< C_SceneEntity::QueuedEvents_t > m_QueuedEvents; // Size: 24
    float32 m_flCurrentTime; 
};

struct  C_SunGlowOverlay {
    char m_pad[208];
    bool m_bModulateByDot; 
};

struct __declspec(align(8))  C_Sun {
    char m_pad[3368];
    ParticleIndex_t m_fxSSSunFlareEffectIndex; 
    ParticleIndex_t m_fxSunFlareEffectIndex; 
    float32 m_fdistNormalize; 
    Vector m_vSunPos; // Size: 12
    Vector m_vDirection; // Size: 16
    CUtlSymbolLarge m_iszEffectName; // Size: 8
    CUtlSymbolLarge m_iszSSEffectName; // Size: 8
    Color m_clrOverlay; 
    bool m_bOn; 
    char m_pad2_3432[2];
    bool m_bmaxColor; 
    float32 m_flSize; 
    float32 m_flHazeScale; 
    float32 m_flRotation; 
    float32 m_flHDRColorScale; 
    float32 m_flAlphaHaze; 
    float32 m_flAlphaScale; 
    float32 m_flAlphaHdr; 
    float32 m_flFarZScale; 
};

struct __declspec(align(8))  C_BaseTrigger {
    char m_pad[3368];
    bool m_bDisabled; 
    bool m_bClientSidePredicted; 
};

struct __declspec(align(8))  C_TriggerVolume {
};

struct __declspec(align(8))  C_TriggerMultiple {
};

struct __declspec(align(8))  C_TriggerLerpObject {
};

struct __declspec(align(8))  C_TriggerPhysics {
    char m_pad[3376];
    float32 m_gravityScale; 
    float32 m_linearLimit; 
    float32 m_linearDamping; 
    float32 m_angularLimit; 
    float32 m_angularDamping; 
    float32 m_linearForce; 
    float32 m_flFrequency; 
    float32 m_flDampingRatio; 
    Vector m_vecLinearForcePointAt; // Size: 12
    char m_pad3_3424[3];
    bool m_bCollapseToForcePoint; 
    Vector m_vecLinearForcePointAtWorld; // Size: 12
    Vector m_vecLinearForceDirection; // Size: 12
    bool m_bConvertToDebrisWhenPossible; 
};

struct __declspec(align(8))  C_Beam {
    char m_pad[3368];
    float32 m_flFrameRate; 
    float32 m_flHDRColorScale; 
    GameTime_t m_flFireTime; 
    float32 m_flDamage; 
    char m_pad3_3388[3];
    uint8 m_nNumBeamEnts; 
    char m_pad32_3424[32];
    int32 m_queryHandleHalo; // Size: 36
    CStrongHandle< InfoForResourceTypeIMaterial2 > m_hBaseMaterial; // Size: 8
    CStrongHandle< InfoForResourceTypeIMaterial2 > m_nHaloIndex; // Size: 8
    BeamType_t m_nBeamType; 
    uint32 m_nBeamFlags; 
    CHandle< C_BaseEntity >[10] m_hAttachEntity; // Size: 40
    AttachmentHandle_t[10] m_nAttachIndex; // Size: 12
    float32 m_fWidth; 
    float32 m_fEndWidth; 
    float32 m_fFadeLength; 
    float32 m_fHaloScale; 
    float32 m_fAmplitude; 
    float32 m_fStartFrame; 
    float32 m_fSpeed; 
    float32 m_flFrame; 
    BeamClipStyle_t m_nClipStyle; 
    char m_pad3_3540[3];
    bool m_bTurnedOff; 
    Vector m_vecEndPos; // Size: 12
    CHandle< C_BaseEntity > m_hEndEntity; 
};

struct __declspec(align(8))  C_FuncLadder {
    char m_pad[3368];
    Vector m_vecLadderDir; // Size: 16
    CUtlVector< CHandle< C_InfoLadderDismount > > m_Dismounts; // Size: 24
    Vector m_vecLocalTop; // Size: 12
    Vector m_vecPlayerMountPositionTop; // Size: 12
    Vector m_vecPlayerMountPositionBottom; // Size: 12
    float32 m_flAutoRideSpeed; 
    bool m_bDisabled; 
    bool m_bFakeLadder; 
    bool m_bHasSlack; 
};

struct __declspec(align(8))  CPrecipitationVData {
    char m_pad[40];
    CResourceNameTyped< CWeakHandle< InfoForResourceTypeIParticleSystemDefinition > > m_szParticlePrecipitationEffect; // Size: 224
    float32 m_flInnerDistance; 
    ParticleAttachment_t m_nAttachType; 
    char m_pad3_276[3];
    bool m_bBatchSameVolumeType; 
    int32 m_nRTEnvCP; 
    char m_pad4_288[4];
    int32 m_nRTEnvCPComponent; // Size: 8
    CUtlString m_szModifier; 
};

struct __declspec(align(8))  C_Sprite {
    char m_pad[3368];
    CStrongHandle< InfoForResourceTypeIMaterial2 > m_hSpriteMaterial; // Size: 8
    CHandle< C_BaseEntity > m_hAttachedToEntity; 
    AttachmentHandle_t m_nAttachment; 
    float32 m_flSpriteFramerate; 
    float32 m_flFrame; 
    GameTime_t m_flDieTime; // Size: 16
    uint32 m_nBrightness; 
    float32 m_flBrightnessDuration; 
    float32 m_flSpriteScale; 
    float32 m_flScaleDuration; 
    char m_pad3_3428[3];
    bool m_bWorldSpaceScale; 
    float32 m_flGlowProxySize; 
    float32 m_flHDRColorScale; 
    GameTime_t m_flLastTime; 
    float32 m_flMaxFrame; 
    float32 m_flStartScale; 
    float32 m_flDestScale; 
    GameTime_t m_flScaleTimeStart; 
    int32 m_nStartBrightness; 
    int32 m_nDestBrightness; 
    GameTime_t m_flBrightnessTimeStart; // Size: 8
    CWeakHandle< InfoForResourceTypeIMaterial2 > m_hOldSpriteMaterial; // Size: 160
    int32 m_nSpriteWidth; 
    int32 m_nSpriteHeight; 
};

struct __declspec(align(8))  CSpriteOriented {
};

struct  C_BaseClientUIEntity {
    char m_pad[3376];
    char m_pad7_3384[7];
    bool m_bEnabled; // Size: 8
    CUtlSymbolLarge m_DialogXMLName; // Size: 8
    CUtlSymbolLarge m_PanelClassName; // Size: 8
    CUtlSymbolLarge m_PanelID; 
};

struct __declspec(align(8))  C_PointClientUIDialog {
    char m_pad[3416];
    CHandle< C_BaseEntity > m_hActivator; 
    bool m_bStartEnabled; 
};

struct __declspec(align(8))  C_PointClientUIHUD {
    char m_pad[3424];
    char m_pad383_3808[383];
    bool m_bCheckCSSClasses; // Size: 384
    char m_pad3_3812[3];
    bool m_bIgnoreInput; 
    float32 m_flWidth; 
    float32 m_flHeight; 
    float32 m_flDPI; 
    float32 m_flInteractDistance; 
    float32 m_flDepthOffset; 
    uint32 m_unOwnerContext; 
    uint32 m_unHorizontalAlign; 
    uint32 m_unVerticalAlign; 
    uint32 m_unOrientation; 
    char m_pad7_3856[7];
    bool m_bAllowInteractionFromAllSceneWorlds; // Size: 8
    C_NetworkUtlVectorBase< CUtlSymbolLarge > m_vecCSSClasses; 
};

struct __declspec(align(16))  CPointOffScreenIndicatorUi {
    char m_pad[3984];
    bool m_bBeenEnabled; 
    char m_pad2_3988[2];
    bool m_bHide; 
    float32 m_flSeenTargetTime; 
    C_PointClientUIWorldPanel* m_pTargetPanel; 
};

struct __declspec(align(16))  C_PointClientUIWorldPanel {
    char m_pad[3424];
    bool m_bForceRecreateNextUpdate; 
    bool m_bMoveViewToPlayerNextThink; 
    char m_pad13_3440[13];
    bool m_bCheckCSSClasses; // Size: 14
    CTransform m_anchorDeltaTransform; // Size: 408
    CPointOffScreenIndicatorUi* m_pOffScreenIndicator; // Size: 40
    bool m_bIgnoreInput; 
    bool m_bLit; 
    char m_pad1_3892[1];
    bool m_bFollowPlayerAcrossTeleport; 
    float32 m_flWidth; 
    float32 m_flHeight; 
    float32 m_flDPI; 
    float32 m_flInteractDistance; 
    float32 m_flDepthOffset; 
    uint32 m_unOwnerContext; 
    uint32 m_unHorizontalAlign; 
    uint32 m_unVerticalAlign; 
    uint32 m_unOrientation; 
    char m_pad7_3936[7];
    bool m_bAllowInteractionFromAllSceneWorlds; // Size: 8
    C_NetworkUtlVectorBase< CUtlSymbolLarge > m_vecCSSClasses; // Size: 24
    bool m_bOpaque; 
    bool m_bNoDepth; 
    bool m_bRenderBackface; 
    bool m_bUseOffScreenIndicator; 
    bool m_bExcludeFromSaveGames; 
    bool m_bGrabbable; 
    bool m_bOnlyRenderToTexture; 
    bool m_bDisableMipGen; 
    int32 m_nExplicitImageLayout; 
};

struct __declspec(align(16))  C_PointClientUIWorldTextPanel {
    char m_pad[3984];
    char[512] m_messageText; 
};

struct __declspec(align(8))  CInfoOffscreenPanoramaTexture {
    char m_pad[1384];
    char m_pad3_1388[3];
    bool m_bDisabled; 
    int32 m_nResolutionX; 
    char m_pad4_1400[4];
    int32 m_nResolutionY; // Size: 8
    CUtlSymbolLarge m_szLayoutFileName; // Size: 8
    CUtlSymbolLarge m_RenderAttrName; // Size: 8
    C_NetworkUtlVectorBase< CHandle< C_BaseModelEntity > > m_TargetEntities; // Size: 24
    char m_pad4_1448[4];
    int32 m_nTargetChangeCount; // Size: 8
    C_NetworkUtlVectorBase< CUtlSymbolLarge > m_vecCSSClasses; // Size: 376
    bool m_bCheckCSSClasses; 
};

struct __declspec(align(8))  CBombTarget {
    char m_pad[3376];
    bool m_bBombPlantedHere; 
};

struct __declspec(align(8))  CHostageRescueZoneShim {
};

struct __declspec(align(8))  CHostageRescueZone {
};

struct __declspec(align(8))  C_TriggerBuoyancy {
    char m_pad[3376];
    CBuoyancyHelper m_BuoyancyHelper; // Size: 128
    float32 m_flFluidDensity; 
};

struct __declspec(align(8))  CFuncWater {
    char m_pad[3368];
    CBuoyancyHelper m_BuoyancyHelper; 
};

struct __declspec(align(8))  CWaterSplasher {
};

struct __declspec(align(8))  C_InfoInstructorHintHostageRescueZone {
};

struct __declspec(align(8))  C_CSObserverPawn {
    char m_pad[5392];
    CEntityHandle m_hDetectParentChange; 
};

struct __declspec(align(8))  C_FootstepControl {
    char m_pad[3376];
    CUtlSymbolLarge m_source; // Size: 8
    CUtlSymbolLarge m_destination; 
};

struct __declspec(align(8))  CCSWeaponBaseVData {
    char m_pad[840];
    CSWeaponType m_WeaponType; 
    CSWeaponCategory m_WeaponCategory; 
    CResourceNameTyped< CWeakHandle< InfoForResourceTypeCModel > > m_szViewModel; // Size: 224
    CResourceNameTyped< CWeakHandle< InfoForResourceTypeCModel > > m_szPlayerModel; // Size: 224
    CResourceNameTyped< CWeakHandle< InfoForResourceTypeCModel > > m_szWorldDroppedModel; // Size: 224
    CResourceNameTyped< CWeakHandle< InfoForResourceTypeCModel > > m_szAimsightLensMaskModel; // Size: 224
    CResourceNameTyped< CWeakHandle< InfoForResourceTypeCModel > > m_szMagazineModel; // Size: 224
    CResourceNameTyped< CWeakHandle< InfoForResourceTypeIParticleSystemDefinition > > m_szHeatEffect; // Size: 224
    CResourceNameTyped< CWeakHandle< InfoForResourceTypeIParticleSystemDefinition > > m_szEjectBrassEffect; // Size: 224
    CResourceNameTyped< CWeakHandle< InfoForResourceTypeIParticleSystemDefinition > > m_szMuzzleFlashParticleAlt; // Size: 224
    CResourceNameTyped< CWeakHandle< InfoForResourceTypeIParticleSystemDefinition > > m_szMuzzleFlashThirdPersonParticle; // Size: 224
    CResourceNameTyped< CWeakHandle< InfoForResourceTypeIParticleSystemDefinition > > m_szMuzzleFlashThirdPersonParticleAlt; // Size: 224
    CResourceNameTyped< CWeakHandle< InfoForResourceTypeIParticleSystemDefinition > > m_szTracerParticle; // Size: 224
    gear_slot_t m_GearSlot; 
    int32 m_GearSlotPosition; 
    loadout_slot_t m_DefaultLoadoutSlot; // Size: 8
    CUtlString m_sWrongTeamMsg; // Size: 8
    int32 m_nPrice; 
    int32 m_nKillAward; 
    int32 m_nPrimaryReserveAmmoMax; 
    int32 m_nSecondaryReserveAmmoMax; 
    bool m_bMeleeWeapon; 
    bool m_bHasBurstMode; 
    bool m_bIsRevolver; 
    char m_pad4_3360[4];
    bool m_bCannotShootUnderwater; 
    CGlobalSymbol m_szName; // Size: 8
    CUtlString m_szAnimExtension; // Size: 8
    CSWeaponSilencerType m_eSilencerType; 
    int32 m_nCrosshairMinDistance; 
    int32 m_nCrosshairDeltaDistance; 
    char m_pad3_3392[3];
    bool m_bIsFullAuto; 
    int32 m_nNumBullets; 
    CFiringModeFloat m_flCycleTime; // Size: 8
    CFiringModeFloat m_flMaxSpeed; // Size: 8
    CFiringModeFloat m_flSpread; // Size: 8
    CFiringModeFloat m_flInaccuracyCrouch; // Size: 8
    CFiringModeFloat m_flInaccuracyStand; // Size: 8
    CFiringModeFloat m_flInaccuracyJump; // Size: 8
    CFiringModeFloat m_flInaccuracyLand; // Size: 8
    CFiringModeFloat m_flInaccuracyLadder; // Size: 8
    CFiringModeFloat m_flInaccuracyFire; // Size: 8
    CFiringModeFloat m_flInaccuracyMove; // Size: 8
    CFiringModeFloat m_flRecoilAngle; // Size: 8
    CFiringModeFloat m_flRecoilAngleVariance; // Size: 8
    CFiringModeFloat m_flRecoilMagnitude; // Size: 8
    CFiringModeFloat m_flRecoilMagnitudeVariance; // Size: 8
    CFiringModeInt m_nTracerFrequency; // Size: 8
    float32 m_flInaccuracyJumpInitial; 
    float32 m_flInaccuracyJumpApex; 
    float32 m_flInaccuracyReload; 
    int32 m_nRecoilSeed; 
    int32 m_nSpreadSeed; 
    float32 m_flTimeToIdleAfterFire; 
    float32 m_flIdleInterval; 
    float32 m_flAttackMovespeedFactor; 
    float32 m_flHeatPerShot; 
    float32 m_flInaccuracyPitchShift; 
    float32 m_flInaccuracyAltSoundThreshold; 
    char m_pad4_3568[4];
    float32 m_flBotAudibleRange; // Size: 8
    CUtlString m_szUseRadioSubtitle; // Size: 8
    bool m_bUnzoomsAfterShot; 
    char m_pad2_3580[2];
    bool m_bHideViewModelWhenZoomed; 
    int32 m_nZoomLevels; 
    int32 m_nZoomFOV1; 
    int32 m_nZoomFOV2; 
    float32 m_flZoomTime0; 
    float32 m_flZoomTime1; 
    float32 m_flZoomTime2; 
    float32 m_flIronSightPullUpSpeed; 
    float32 m_flIronSightPutDownSpeed; 
    float32 m_flIronSightFOV; 
    float32 m_flIronSightPivotForward; 
    float32 m_flIronSightLooseness; 
    QAngle m_angPivotAngle; // Size: 12
    Vector m_vecIronSightEyePos; // Size: 12
    int32 m_nDamage; 
    float32 m_flHeadshotMultiplier; 
    float32 m_flArmorRatio; 
    float32 m_flPenetration; 
    float32 m_flRange; 
    float32 m_flRangeModifier; 
    float32 m_flFlinchVelocityModifierLarge; 
    float32 m_flFlinchVelocityModifierSmall; 
    float32 m_flRecoveryTimeCrouch; 
    float32 m_flRecoveryTimeStand; 
    float32 m_flRecoveryTimeCrouchFinal; 
    float32 m_flRecoveryTimeStandFinal; 
    int32 m_nRecoveryTransitionStartBullet; 
    int32 m_nRecoveryTransitionEndBullet; 
    float32 m_flThrowVelocity; 
    Vector m_vSmokeColor; // Size: 12
    CGlobalSymbol m_szAnimClass; 
};

struct __declspec(align(8))  C_PlayerSprayDecal {
    char m_pad[3368];
    int32 m_nUniqueID; 
    uint32 m_unAccountID; 
    uint32 m_unTraceID; 
    uint32 m_rtGcTime; 
    Vector m_vecEndPos; // Size: 12
    Vector m_vecStart; // Size: 12
    Vector m_vecLeft; // Size: 12
    Vector m_vecNormal; // Size: 12
    int32 m_nPlayer; 
    int32 m_nEntity; 
    int32 m_nHitbox; 
    float32 m_flCreationTime; 
    int32 m_nTintID; 
    uint8 m_nVersion; 
    uint8[128] m_ubSignature; // Size: 139
    CPlayerSprayDecalRenderHelper m_SprayRenderHelper; 
};

struct __declspec(align(8))  C_FuncConveyor {
    char m_pad[3376];
    Vector m_vecMoveDirEntitySpace; // Size: 12
    float32 m_flTargetSpeed; 
    GameTick_t m_nTransitionStartTick; 
    int32 m_nTransitionDurationTicks; 
    char m_pad4_3408[4];
    float32 m_flTransitionStartSpeed; // Size: 8
    C_NetworkUtlVectorBase< CHandle< C_BaseEntity > > m_hConveyorModels; // Size: 24
    float32 m_flCurrentConveyorOffset; 
    float32 m_flCurrentConveyorSpeed; 
};

struct __declspec(align(16))  CGrenadeTracer {
    char m_pad[3392];
    float32 m_flTracerDuration; 
    GrenadeType_t m_nType; 
};

struct __declspec(align(16))  C_Inferno {
    char m_pad[3432];
    ParticleIndex_t m_nfxFireDamageEffect; // Size: 8
    CStrongHandle< InfoForResourceTypeIParticleSnapshot > m_hInfernoPointsSnapshot; // Size: 8
    CStrongHandle< InfoForResourceTypeIParticleSnapshot > m_hInfernoFillerPointsSnapshot; // Size: 8
    CStrongHandle< InfoForResourceTypeIParticleSnapshot > m_hInfernoOutlinePointsSnapshot; // Size: 8
    CStrongHandle< InfoForResourceTypeIParticleSnapshot > m_hInfernoClimbingOutlinePointsSnapshot; // Size: 8
    CStrongHandle< InfoForResourceTypeIParticleSnapshot > m_hInfernoDecalsSnapshot; // Size: 8
    Vector[64] m_firePositions; // Size: 768
    Vector[64] m_fireParentPositions; // Size: 768
    bool[64] m_bFireIsBurning; // Size: 64
    Vector[64] m_BurnNormal; // Size: 768
    int32 m_fireCount; 
    int32 m_nInfernoType; 
    float32 m_nFireLifetime; 
    char m_pad3_5864[3];
    bool m_bInPostEffectTime; 
    int32 m_lastFireCount; 
    char m_pad27648_33520[27648];
    int32 m_nFireEffectTickBegin; // Size: 27652
    int32 m_drawableCount; 
    char m_pad3_33528[3];
    bool m_blosCheck; 
    int32 m_nlosperiod; 
    float32 m_maxFireHalfWidth; 
    float32 m_maxFireHeight; 
    Vector m_minBounds; // Size: 12
    Vector m_maxBounds; // Size: 12
    float32 m_flLastGrassBurnThink; 
};

struct __declspec(align(16))  C_FireCrackerBlast {
};

struct __declspec(align(8))  C_BarnLight {
    char m_pad[3368];
    char m_pad3_3372[3];
    bool m_bEnabled; 
    int32 m_nColorMode; 
    Color m_Color; 
    float32 m_flColorTemperature; 
    float32 m_flBrightness; 
    float32 m_flBrightnessScale; 
    int32 m_nDirectLight; 
    int32 m_nBakedShadowIndex; 
    int32 m_nLuminaireShape; 
    float32 m_flLuminaireSize; 
    char m_pad4_3416[4];
    float32 m_flLuminaireAnisotropy; // Size: 8
    CUtlString m_LightStyleString; // Size: 8
    GameTime_t m_flLightStyleStartTime; // Size: 8
    C_NetworkUtlVectorBase< CUtlString > m_QueuedLightStyleStrings; // Size: 24
    C_NetworkUtlVectorBase< CUtlString > m_LightStyleEvents; // Size: 24
    C_NetworkUtlVectorBase< CHandle< C_BaseModelEntity > > m_LightStyleTargets; // Size: 24
    CEntityIOOutput[4] m_StyleEvent; // Size: 160
    CStrongHandle< InfoForResourceTypeCTextureBase > m_hLightCookie; // Size: 8
    float32 m_flShape; 
    float32 m_flSoftX; 
    float32 m_flSoftY; 
    float32 m_flSkirt; 
    float32 m_flSkirtNear; 
    Vector m_vSizeParams; // Size: 12
    float32 m_flRange; 
    Vector m_vShear; // Size: 12
    int32 m_nBakeSpecularToCubemaps; 
    Vector m_vBakeSpecularToCubemapsSize; // Size: 12
    int32 m_nCastShadows; 
    int32 m_nShadowMapSize; 
    int32 m_nShadowPriority; 
    char m_pad3_3752[3];
    bool m_bContactShadow; 
    int32 m_nBounceLight; 
    float32 m_flBounceScale; 
    float32 m_flMinRoughness; 
    Vector m_vAlternateColor; // Size: 12
    float32 m_fAlternateColorBrightness; 
    int32 m_nFog; 
    float32 m_flFogStrength; 
    int32 m_nFogShadows; 
    float32 m_flFogScale; 
    char m_pad3_3800[3];
    bool m_bFogMixedShadows; 
    float32 m_flFadeSizeStart; 
    float32 m_flFadeSizeEnd; 
    float32 m_flShadowFadeSizeStart; 
    float32 m_flShadowFadeSizeEnd; 
    char m_pad3_3820[3];
    bool m_bPrecomputedFieldsValid; 
    Vector m_vPrecomputedBoundsMins; // Size: 12
    Vector m_vPrecomputedBoundsMaxs; // Size: 12
    Vector m_vPrecomputedOBBOrigin; // Size: 12
    QAngle m_vPrecomputedOBBAngles; // Size: 12
    Vector m_vPrecomputedOBBExtent; // Size: 12
    int32 m_nPrecomputedSubFrusta; 
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
    char m_pad7_4176[7];
    bool m_bInitialBoneSetup; // Size: 8
    C_NetworkUtlVectorBase< uint16 > m_VisClusters; 
};

struct __declspec(align(8))  C_RectLight {
    char m_pad[4208];
    bool m_bShowLight; 
};

struct __declspec(align(8))  C_OmniLight {
    char m_pad[4208];
    float32 m_flInnerAngle; 
    float32 m_flOuterAngle; 
    bool m_bShowLight; 
};

struct __declspec(align(8))  C_CSTeam {
    char m_pad[1568];
    char[512] m_szTeamMatchStat; // Size: 512
    int32 m_numMapVictories; 
    char m_pad3_2088[3];
    bool m_bSurrendered; 
    int32 m_scoreFirstHalf; 
    int32 m_scoreSecondHalf; 
    int32 m_scoreOvertime; 
    char[129] m_szClanTeamname; // Size: 132
    uint32 m_iClanID; 
    char[8] m_szTeamFlagImage; // Size: 8
    char[8] m_szTeamLogoImage; 
};

struct __declspec(align(8))  C_MapPreviewParticleSystem {
};

struct __declspec(align(8))  CInfoDynamicShadowHint {
    char m_pad[1384];
    char m_pad3_1388[3];
    bool m_bDisabled; 
    float32 m_flRange; 
    int32 m_nImportance; 
    int32 m_nLightChoice; 
    CHandle< C_BaseEntity > m_hLight; 
};

struct __declspec(align(8))  CInfoDynamicShadowHintBox {
    char m_pad[1408];
    Vector m_vBoxMins; // Size: 12
    Vector m_vBoxMaxs; 
};

struct __declspec(align(8))  C_EnvSky {
    char m_pad[3368];
    CStrongHandle< InfoForResourceTypeIMaterial2 > m_hSkyMaterial; // Size: 8
    CStrongHandle< InfoForResourceTypeIMaterial2 > m_hSkyMaterialLightingOnly; // Size: 8
    bool m_bStartDisabled; 
    Color m_vTintColor; 
    Color m_vTintColorLightingOnly; 
    float32 m_flBrightnessScale; 
    int32 m_nFogType; 
    float32 m_flFogMinStart; 
    float32 m_flFogMinEnd; 
    float32 m_flFogMaxStart; 
    float32 m_flFogMaxEnd; 
    bool m_bEnabled; 
};

struct __declspec(align(8))  C_TonemapController2Alias_env_tonemap_controller2 {
};

struct __declspec(align(8))  C_LightEntity {
    char m_pad[3368];
    CLightComponent* m_CLightComponent; 
};

struct __declspec(align(8))  C_LightSpotEntity {
};

struct __declspec(align(8))  C_LightOrthoEntity {
};

struct __declspec(align(8))  C_LightDirectionalEntity {
};

struct __declspec(align(8))  C_LightEnvironmentEntity {
};

struct __declspec(align(8))  C_EnvParticleGlow {
    char m_pad[4824];
    float32 m_flAlphaScale; 
    float32 m_flRadiusScale; 
    float32 m_flSelfIllumScale; 
    Color m_ColorTint; 
    CStrongHandle< InfoForResourceTypeCTextureBase > m_hTextureOverride; 
};

struct __declspec(align(8))  C_TextureBasedAnimatable {
    char m_pad[3368];
    char m_pad3_3372[3];
    bool m_bLoop; 
    float32 m_flFPS; 
    CStrongHandle< InfoForResourceTypeCTextureBase > m_hPositionKeys; // Size: 8
    CStrongHandle< InfoForResourceTypeCTextureBase > m_hRotationKeys; // Size: 8
    Vector m_vAnimationBoundsMin; // Size: 12
    Vector m_vAnimationBoundsMax; // Size: 12
    float32 m_flStartTime; 
    float32 m_flStartFrame; 
};

struct __declspec(align(8))  C_World {
};

struct __declspec(align(8))  CBaseProp {
    char m_pad[3976];
    char m_pad3_3980[3];
    bool m_bModelOverrodeBlockLOS; 
    int32 m_iShapeType; 
    char m_pad3_3988[3];
    bool m_bConformToCollisionBounds; 
    matrix3x4_t m_mPreferredCatchTransform; 
};

struct __declspec(align(8))  C_BreakableProp {
    char m_pad[4040];
    CPropDataComponent m_CPropDataComponent; // Size: 64
    CEntityIOOutput m_OnBreak; // Size: 40
    CEntityOutputTemplate< float32 > m_OnHealthChanged; // Size: 40
    CEntityIOOutput m_OnTakeDamage; // Size: 40
    float32 m_impactEnergyScale; 
    int32 m_iMinHealthDmg; 
    float32 m_flPressureDelay; 
    float32 m_flDefBurstScale; 
    Vector m_vDefBurstOffset; // Size: 12
    CHandle< C_BaseEntity > m_hBreaker; 
    PerformanceMode_t m_PerformanceMode; 
    GameTime_t m_flPreventDamageBeforeTime; 
    BreakableContentsType_t m_BreakableContentsType; // Size: 8
    CUtlString m_strBreakableContentsPropGroupOverride; // Size: 8
    CUtlString m_strBreakableContentsParticleOverride; // Size: 8
    char m_pad3_4292[3];
    bool m_bHasBreakPiecesOrCommands; 
    float32 m_explodeDamage; 
    char m_pad4_4304[4];
    float32 m_explodeRadius; // Size: 8
    char m_pad4_4312[4];
    float32 m_explosionDelay; // Size: 8
    CUtlSymbolLarge m_explosionBuildupSound; // Size: 8
    CUtlSymbolLarge m_explosionCustomEffect; // Size: 8
    CUtlSymbolLarge m_explosionCustomSound; // Size: 8
    CUtlSymbolLarge m_explosionModifier; // Size: 8
    CHandle< C_BasePlayerPawn > m_hPhysicsAttacker; 
    GameTime_t m_flLastPhysicsInfluenceTime; 
    float32 m_flDefaultFadeScale; 
    CHandle< C_BaseEntity > m_hLastAttacker; 
    CHandle< C_BaseEntity > m_hFlareEnt; 
    bool m_noGhostCollision; 
};

struct __declspec(align(8))  C_DynamicProp {
    char m_pad[4368];
    bool m_bUseHitboxesForRenderBox; 
    char m_pad6_4376[6];
    bool m_bUseAnimGraph; 
    CEntityIOOutput m_pOutputAnimBegun; // Size: 40
    CEntityIOOutput m_pOutputAnimOver; // Size: 40
    CEntityIOOutput m_pOutputAnimLoopCycleOver; // Size: 40
    CEntityIOOutput m_OnAnimReachedStart; // Size: 40
    CEntityIOOutput m_OnAnimReachedEnd; // Size: 40
    CUtlSymbolLarge m_iszIdleAnim; // Size: 8
    AnimLoopMode_t m_nIdleAnimLoopMode; 
    bool m_bRandomizeCycle; 
    bool m_bStartDisabled; 
    bool m_bFiredStartEndOutput; 
    bool m_bForceNpcExclude; 
    bool m_bCreateNonSolid; 
    char m_pad2_4596[2];
    bool m_bIsOverrideProp; 
    int32 m_iInitialGlowState; 
    int32 m_nGlowRange; 
    int32 m_nGlowRangeMin; 
    Color m_glowColor; 
    int32 m_nGlowTeam; 
    int32 m_iCachedFrameCount; 
    Vector m_vecCachedRenderMins; // Size: 12
    Vector m_vecCachedRenderMaxs; 
};

struct __declspec(align(8))  C_DynamicPropAlias_dynamic_prop {
};

struct __declspec(align(8))  C_DynamicPropAlias_prop_dynamic_override {
};

struct __declspec(align(8))  C_DynamicPropAlias_cable_dynamic {
};

struct __declspec(align(8))  C_ColorCorrectionVolume {
    char m_pad[3376];
    float32 m_LastEnterWeight; 
    float32 m_LastEnterTime; 
    float32 m_LastExitWeight; 
    float32 m_LastExitTime; 
    char m_pad3_3396[3];
    bool m_bEnabled; 
    float32 m_MaxWeight; 
    float32 m_FadeDuration; 
    float32 m_Weight; 
    char[512] m_lookupFilename; 
};

struct __declspec(align(16))  C_FuncMonitor {
    char m_pad[3368];
    CUtlString m_targetCamera; // Size: 8
    int32 m_nResolutionEnum; 
    bool m_bRenderShadows; 
    char m_pad2_3384[2];
    bool m_bUseUniqueColorTarget; 
    CUtlString m_brushModelName; // Size: 8
    CHandle< C_BaseEntity > m_hTargetCamera; 
    bool m_bEnabled; 
    bool m_bDraw3DSkybox; 
};

struct __declspec(align(8))  C_FuncMoveLinear {
};

struct __declspec(align(8))  C_FuncMover {
};

struct __declspec(align(8))  C_PhysMagnet {
    char m_pad[3976];
    CUtlVector< int32 > m_aAttachedObjectsFromServer; // Size: 24
    CUtlVector< CHandle< C_BaseEntity > > m_aAttachedObjects; 
};

struct __declspec(align(8))  C_PointCommentaryNode {
    char m_pad[3984];
    bool m_bActive; 
    char m_pad2_3988[2];
    bool m_bWasActive; 
    GameTime_t m_flEndTime; 
    GameTime_t m_flStartTime; 
    float32 m_flStartTimeInCommentary; 
    CUtlSymbolLarge m_iszCommentaryFile; // Size: 8
    CUtlSymbolLarge m_iszTitle; // Size: 8
    CUtlSymbolLarge m_iszSpeakers; // Size: 8
    int32 m_iNodeNumber; 
    int32 m_iNodeNumberMax; 
    char m_pad15_4048[15];
    bool m_bListenedTo; // Size: 16
    CHandle< C_BaseEntity > m_hViewPosition; 
    bool m_bRestartAfterRestore; 
};

struct __declspec(align(8))  C_WaterBullet {
};

struct __declspec(align(8))  C_BaseDoor {
    char m_pad[3368];
    bool m_bIsUsable; 
};

struct __declspec(align(8))  C_ClientRagdoll {
    char m_pad[3976];
    bool m_bFadeOut; 
    char m_pad2_3980[2];
    bool m_bImportant; 
    GameTime_t m_flEffectTime; 
    GameTime_t m_gibDespawnTime; 
    int32 m_iCurrentFriction; 
    int32 m_iMinFriction; 
    int32 m_iMaxFriction; 
    int32 m_iFrictionAnimState; 
    bool m_bReleaseRagdoll; 
    AttachmentHandle_t m_iEyeAttachment; 
    char m_pad1_4008[1];
    bool m_bFadingOut; 
    float32[10] m_flScaleEnd; // Size: 40
    GameTime_t[10] m_flScaleTimeStart; // Size: 40
    GameTime_t[10] m_flScaleTimeEnd; 
};

struct __declspec(align(8))  C_Precipitation {
    char m_pad[3376];
    char m_pad12_3392[12];
    float32 m_flDensity; // Size: 16
    char m_pad4_3400[4];
    float32 m_flParticleInnerDist; // Size: 8
    char* m_pParticleDef; // Size: 40
    TimedEvent[1] m_tParticlePrecipTraceTimer; // Size: 8
    bool[1] m_bActiveParticlePrecipEmitter; 
    bool m_bParticlePrecipInitialized; 
    char m_pad1_3452[1];
    bool m_bHasSimulatedSinceLastSceneObjectUpdate; 
    int32 m_nAvailableSheetSequencesMaxIndex; 
};

struct __declspec(align(8))  C_FireSprite {
    char m_pad[3640];
    Vector m_vecMoveDir; // Size: 12
    bool m_bFadeFromAbove; 
};

struct __declspec(align(8))  C_FireFromAboveSprite {
};

struct __declspec(align(8))  C_Fish {
    char m_pad[3976];
    Vector m_pos; // Size: 12
    Vector m_vel; // Size: 12
    QAngle m_angles; // Size: 12
    int32 m_localLifeState; 
    float32 m_deathDepth; 
    float32 m_deathAngle; 
    char m_pad4_4032[4];
    float32 m_buoyancy; // Size: 8
    CountdownTimer m_wiggleTimer; // Size: 24
    float32 m_wigglePhase; 
    float32 m_wiggleRate; 
    Vector m_actualPos; // Size: 12
    QAngle m_actualAngles; // Size: 12
    Vector m_poolOrigin; // Size: 12
    float32 m_waterLevel; 
    char m_pad3_4108[3];
    bool m_gotUpdate; 
    float32 m_x; 
    float32 m_y; 
    float32 m_z; 
    float32 m_angle; 
    float32[20] m_errorHistory; // Size: 80
    int32 m_errorHistoryIndex; 
    int32 m_errorHistoryCount; 
    float32 m_averageError; 
};

struct __declspec(align(8))  C_PhysicsProp {
    char m_pad[4368];
    bool m_bAwake; 
};

struct __declspec(align(8))  C_BasePropDoor {
    char m_pad[4664];
    DoorState_t m_eDoorState; 
    bool m_modelChanged; 
    char m_pad2_4672[2];
    bool m_bLocked; 
    Vector m_closedPosition; // Size: 12
    QAngle m_closedAngles; // Size: 12
    CHandle< C_BasePropDoor > m_hMaster; 
    Vector m_vWhereToSetLightingOrigin; 
};

struct __declspec(align(8))  C_PropDoorRotating {
};

struct __declspec(align(8))  C_PhysPropClientside {
    char m_pad[4368];
    GameTime_t m_flTouchDelta; 
    GameTime_t m_fDeathTime; 
    float32 m_inertiaScale; 
    Vector m_vecDamagePosition; // Size: 12
    Vector m_vecDamageDirection; // Size: 12
    DamageTypes_t m_nDamageType; 
};

struct __declspec(align(8))  C_RagdollProp {
    char m_pad[3984];
    C_NetworkUtlVectorBase< Vector > m_ragPos; // Size: 24
    C_NetworkUtlVectorBase< QAngle > m_ragAngles; // Size: 24
    float32 m_flBlendWeight; 
    CHandle< C_BaseEntity > m_hRagdollSource; 
    AttachmentHandle_t m_iEyeAttachment; 
    float32 m_flBlendWeightCurrent; 
    CUtlVector< int32 > m_parentPhysicsBoneIndices; // Size: 24
    CUtlVector< int32 > m_worldSpaceBoneComputationOrder; 
};

struct __declspec(align(8))  C_LocalTempEntity {
    char m_pad[3976];
    int32 flags; 
    GameTime_t die; 
    float32 m_flFrameMax; 
    float32 x; 
    float32 y; 
    float32 fadeSpeed; 
    float32 bounceFactor; 
    int32 hitSound; 
    int32 priority; 
    Vector tentOffset; // Size: 12
    QAngle m_vecTempEntAngVelocity; // Size: 12
    int32 tempent_renderamt; 
    Vector m_vecNormal; // Size: 12
    float32 m_flSpriteScale; 
    int32 m_nFlickerFrame; 
    float32 m_flFrameRate; 
    char m_pad4_4072[4];
    float32 m_flFrame; // Size: 8
    char* m_pszImpactEffect; // Size: 8
    char* m_pszParticleEffect; // Size: 8
    char m_pad3_4092[3];
    bool m_bParticleCollision; 
    int32 m_iLastCollisionFrame; 
    Vector m_vLastCollisionOrigin; // Size: 12
    Vector m_vecTempEntVelocity; // Size: 12
    Vector m_vecPrevAbsOrigin; // Size: 12
    Vector m_vecTempEntAcceleration; 
};

struct __declspec(align(8))  C_ShatterGlassShardPhysics {
    char m_pad[4384];
    shard_model_desc_t m_ShardDesc; 
};

struct __declspec(align(8))  C_EconEntity {
    char m_pad[4400];
    char m_pad4_4408[4];
    float32 m_flFlexDelayTime; // Size: 8
    float32* m_flFlexDelayedWeight; // Size: 8
    char m_pad7_4424[7];
    bool m_bAttributesInitialized; // Size: 8
    C_AttributeContainer m_AttributeManager; // Size: 1192
    uint32 m_OriginalOwnerXuidLow; 
    uint32 m_OriginalOwnerXuidHigh; 
    int32 m_nFallbackPaintKit; 
    int32 m_nFallbackSeed; 
    float32 m_flFallbackWear; 
    int32 m_nFallbackStatTrak; 
    bool m_bClientside; 
    char m_pad6_5648[6];
    bool m_bParticleSystemsCreated; 
    CUtlVector< int32 > m_vecAttachedParticles; // Size: 24
    CHandle< CBaseAnimGraph > m_hViewmodelAttachment; 
    int32 m_iOldTeam; 
    char m_pad3_5684[3];
    bool m_bAttachmentDirty; 
    int32 m_nUnloadedModelIndex; 
    char m_pad12_5704[12];
    int32 m_iNumOwnerValidationRetries; // Size: 16
    CHandle< C_BaseEntity > m_hOldProvidee; // Size: 8
    CUtlVector< C_EconEntity::AttachedModelData_t > m_vecAttachedModels; 
};

struct __declspec(align(8))  C_EconWearable {
    char m_pad[5736];
    int32 m_nForceSkin; 
    bool m_bAlwaysAllow; 
};

struct __declspec(align(8))  C_BaseGrenade {
    char m_pad[4384];
    bool m_bHasWarnedAI; 
    bool m_bIsSmokeGrenade; 
    char m_pad1_4388[1];
    bool m_bIsLive; 
    float32 m_DmgRadius; 
    GameTime_t m_flDetonateTime; 
    float32 m_flWarnAITime; 
    char m_pad4_4408[4];
    float32 m_flDamage; // Size: 8
    CUtlSymbolLarge m_iszBounceSound; // Size: 8
    CUtlString m_ExplosionSound; // Size: 12
    CHandle< C_CSPlayerPawn > m_hThrower; // Size: 24
    GameTime_t m_flNextAttack; 
    CHandle< C_CSPlayerPawn > m_hOriginalThrower; 
};

struct __declspec(align(8))  C_PhysicsPropMultiplayer {
};

struct __declspec(align(8))  C_ViewmodelAttachmentModel {
    char m_pad[3984];
    bool m_bShouldFrontFaceCullLeftHanded; 
    bool m_bCreatedLeftHanded; 
};

struct __declspec(align(8))  C_PredictedViewModel {
    char m_pad[4080];
    Vector m_vPredictedLagOffset; // Size: 12
    QAngle m_targetSpeed; // Size: 12
    QAngle m_currentSpeed; 
};

struct __declspec(align(8))  C_CS2WeaponModuleBase {
};

struct __declspec(align(8))  C_StattrakModule {
    char m_pad[3984];
    bool m_bKnife; 
};

struct __declspec(align(8))  C_NametagModule {
    char m_pad[3984];
    CUtlString m_strNametagString; 
};

struct __declspec(align(8))  C_KeychainModule {
    char m_pad[3984];
    uint32 m_nKeychainDefID; 
    uint32 m_nKeychainSeed; 
};

struct __declspec(align(8))  C_BaseCSGrenadeProjectile {
    char m_pad[4464];
    Vector m_vInitialPosition; // Size: 12
    Vector m_vInitialVelocity; // Size: 12
    char m_pad4_4496[4];
    int32 m_nBounces; // Size: 8
    CStrongHandle< InfoForResourceTypeIParticleSystemDefinition > m_nExplodeEffectIndex; // Size: 8
    int32 m_nExplodeEffectTickBegin; 
    Vector m_vecExplodeEffectOrigin; // Size: 12
    GameTime_t m_flSpawnTime; 
    Vector vecLastTrailLinePos; // Size: 12
    GameTime_t flNextTrailLineTime; 
    bool m_bExplodeEffectBegan; 
    char m_pad2_4544[2];
    bool m_bCanCreateGrenadeTrail; 
    ParticleIndex_t m_nSnapshotTrajectoryEffectIndex; // Size: 8
    CStrongHandle< InfoForResourceTypeIParticleSnapshot > m_hSnapshotTrajectoryParticleSnapshot; // Size: 8
    CUtlVector< Vector > m_arrTrajectoryTrailPoints; // Size: 24
    CUtlVector< float32 > m_arrTrajectoryTrailPointCreationTimes; // Size: 24
    float32 m_flTrajectoryTrailEffectCreationTime; 
};

struct __declspec(align(8))  C_SensorGrenadeProjectile {
};

struct __declspec(align(8))  CBreachChargeProjectile {
};

struct __declspec(align(8))  CBumpMineProjectile {
};

struct __declspec(align(8))  CTripWireFireProjectile {
};

struct __declspec(align(8))  C_CSGO_PreviewModel {
    char m_pad[4384];
    CUtlString m_animgraph; // Size: 8
    CGlobalSymbol m_animgraphCharacterModeString; // Size: 8
    CUtlString m_defaultAnim; // Size: 8
    AnimLoopMode_t m_nDefaultAnimLoopMode; 
    float32 m_flInitialModelScale; 
    CUtlString m_sInitialWeaponState; 
};

struct __declspec(align(8))  C_CSGO_PreviewModelAlias_csgo_item_previewmodel {
};

struct __declspec(align(8))  C_WorldModelGloves {
};

struct __declspec(align(8))  C_BulletHitModel {
    char m_pad[3976];
    matrix3x4_t m_matLocal; // Size: 48
    int32 m_iBoneIndex; 
    CHandle< C_BaseEntity > m_hPlayerParent; 
    char m_pad3_4036[3];
    bool m_bIsHit; 
    float32 m_flTimeCreated; 
    Vector m_vecStartPos; 
};

struct __declspec(align(8))  C_HostageCarriableProp {
};

struct __declspec(align(8))  C_PlantedC4 {
    char m_pad[3984];
    char m_pad3_3988[3];
    bool m_bBombTicking; 
    int32 m_nBombSite; 
    char m_pad4_4000[4];
    int32 m_nSourceSoundscapeHash; // Size: 8
    EntitySpottedState_t m_entitySpottedState; // Size: 24
    GameTime_t m_flNextGlow; 
    GameTime_t m_flNextBeep; 
    GameTime_t m_flC4Blow; 
    bool m_bCannotBeDefused; 
    char m_pad2_4040[2];
    bool m_bHasExploded; 
    float32 m_flTimerLength; 
    char m_pad3_4048[3];
    bool m_bBeingDefused; 
    float32 m_bTriggerWarning; 
    float32 m_bExplodeWarning; 
    bool m_bC4Activated; 
    char m_pad2_4060[2];
    bool m_bTenSecWarning; 
    float32 m_flDefuseLength; 
    GameTime_t m_flDefuseCountDown; 
    char m_pad3_4072[3];
    bool m_bBombDefused; 
    CHandle< C_CSPlayerPawn > m_hBombDefuser; 
    CHandle< C_BaseEntity > m_hControlPanel; 
    C_AttributeContainer m_AttributeManager; // Size: 1192
    CHandle< C_Multimeter > m_hDefuserMultimeter; 
    GameTime_t m_flNextRadarFlashTime; 
    char m_pad3_5284[3];
    bool m_bRadarFlash; 
    CHandle< C_CSPlayerPawn > m_pBombDefuser; 
    GameTime_t m_fLastDefuseTime; // Size: 8
    CBasePlayerController* m_pPredictionOwner; // Size: 8
    Vector m_vecC4ExplodeSpectatePos; // Size: 12
    QAngle m_vecC4ExplodeSpectateAng; // Size: 12
    float32 m_flC4ExplodeSpectateDuration; 
};

struct __declspec(align(8))  C_Multimeter {
    char m_pad[3984];
    CHandle< C_PlantedC4 > m_hTargetC4; 
};

struct __declspec(align(8))  C_Item {
    char m_pad[5736];
    char[256] m_pReticleHintTextName; 
};

struct __declspec(align(8))  C_HEGrenadeProjectile {
};

struct __declspec(align(8))  C_FlashbangProjectile {
};

struct __declspec(align(8))  C_Chicken {
    char m_pad[4656];
    CHandle< CBaseAnimGraph > m_hHolidayHatAddon; 
    char m_pad3_4664[3];
    bool m_jumpedThisFrame; 
    CHandle< C_CSPlayerPawn > m_leader; // Size: 8
    C_AttributeContainer m_AttributeManager; // Size: 1192
    char m_pad3_5868[3];
    bool m_bAttributesInitialized; 
    ParticleIndex_t m_hWaterWakeParticles; 
    bool m_bIsPreviewModel; 
};

struct __declspec(align(8))  C_RagdollPropAttached {
    char m_pad[4096];
    uint32 m_boneIndexAttached; 
    uint32 m_ragdollAttachedObjectIndex; 
    Vector m_attachmentPointBoneSpace; // Size: 12
    Vector m_attachmentPointRagdollSpace; // Size: 12
    Vector m_vecOffset; // Size: 12
    float32 m_parentTime; 
    bool m_bHasParent; 
};

struct __declspec(align(8))  C_BaseCombatCharacter {
    char m_pad[4384];
    C_NetworkUtlVectorBase< CHandle< C_EconWearable > > m_hMyWearables; // Size: 24
    AttachmentHandle_t m_leftFootAttachment; 
    AttachmentHandle_t m_rightFootAttachment; 
    C_BaseCombatCharacter::WaterWakeMode_t m_nWaterWakeMode; 
    float32 m_flWaterWorldZ; 
    float32 m_flWaterNextTraceTime; 
};

struct __declspec(align(8))  C_CSGOViewModel {
    char m_pad[4129];
    char m_pad2_4132[2];
    bool m_bShouldIgnoreOffsetAndAccuracy; 
    CEntityIndex m_nLastKnownAssociatedWeaponEntIndex; 
    char m_pad79_4216[79];
    bool m_bNeedToQueueHighResComposite; // Size: 80
    QAngle m_vLoweredWeaponOffset; 
};

struct  C_CSWeaponBase {
    char m_pad[5852];
    float32 m_flFireSequenceStartTime; 
    int32 m_nFireSequenceStartTimeChange; 
    int32 m_nFireSequenceStartTimeAck; 
    PlayerAnimEvent_t m_ePlayerFireEvent; 
    WeaponAttackType_t m_ePlayerFireEventAttackType; 
    HSequence m_seqIdle; 
    HSequence m_seqFirePrimary; 
    HSequence m_seqFireSecondary; // Size: 8
    CUtlVector< HSequence > m_thirdPersonFireSequences; // Size: 24
    HSequence m_hCurrentThirdPersonSequence; 
    int32 m_nSilencerBoneIndex; 
    HSequence[7] m_thirdPersonSequences; // Size: 56
    CSWeaponState_t m_ClientPreviousWeaponState; 
    CSWeaponState_t m_iState; 
    float32 m_flCrosshairDistance; 
    int32 m_iAmmoLastCheck; 
    int32 m_iAlpha; 
    int32 m_iScopeTextureID; 
    int32 m_iCrosshairTextureID; 
    float32 m_flGunAccuracyPositionDeprecated; 
    int32 m_nLastEmptySoundCmdNum; 
    uint32 m_nViewModelIndex; 
    char m_pad3_6020[3];
    bool m_bReloadsWithClips; 
    GameTime_t m_flTimeWeaponIdle; 
    char m_pad7_6032[7];
    bool m_bFireOnEmpty; // Size: 8
    CEntityIOOutput m_OnPlayerPickup; // Size: 40
    CSWeaponMode m_weaponMode; 
    float32 m_flTurningInaccuracyDelta; 
    Vector m_vecTurningInaccuracyEyeDirLast; // Size: 12
    float32 m_flTurningInaccuracy; 
    float32 m_fAccuracyPenalty; 
    GameTime_t m_flLastAccuracyUpdateTime; 
    float32 m_fAccuracySmoothedForZoom; 
    GameTime_t m_fScopeZoomEndTime; 
    int32 m_iRecoilIndex; 
    float32 m_flRecoilIndex; 
    char m_pad3_6124[3];
    bool m_bBurstMode; 
    GameTime_t m_flLastBurstModeChangeTime; 
    GameTick_t m_nPostponeFireReadyTicks; 
    float32 m_flPostponeFireReadyFrac; 
    bool m_bInReload; 
    char m_pad2_6140[2];
    bool m_bReloadVisuallyComplete; 
    GameTime_t m_flDroppedAtTime; 
    bool m_bIsHauledBack; 
    char m_pad2_6148[2];
    bool m_bSilencerOn; 
    GameTime_t m_flTimeSilencerSwitchComplete; 
    int32 m_iOriginalTeamNumber; 
    int32 m_iMostRecentTeamNumber; 
    char m_pad3_6164[3];
    bool m_bDroppedNearBuyZone; 
    char m_pad152_6320[152];
    float32 m_flNextAttackRenderTimeOffset; // Size: 156
    bool m_bClearWeaponIdentifyingUGC; 
    bool m_bVisualsDataSet; 
    bool m_bOldFirstPersonSpectatedState; 
    bool m_bUIWeapon; 
    char m_pad8_6336[8];
    int32 m_nCustomEconReloadEventId; // Size: 12
    CHandle< C_CSPlayerPawn > m_hPrevOwner; 
    GameTick_t m_nDropTick; // Size: 32
    char m_pad3_6376[3];
    bool m_donated; 
    GameTime_t m_fLastShotTime; 
    bool m_bWasOwnedByCT; 
    char m_pad2_6384[2];
    bool m_bWasOwnedByTerrorist; 
    float32 m_gunHeat; 
    uint32 m_smokeAttachments; 
    GameTime_t m_lastSmokeTime; 
    float32 m_flNextClientFireBulletTime; 
    char m_pad220_6624[220];
    float32 m_flNextClientFireBulletTime_Repredict; // Size: 224
    C_IronSightController m_IronSightController; // Size: 176
    char m_pad12_6816[12];
    int32 m_iIronSightMode; // Size: 16
    GameTime_t m_flLastLOSTraceFailureTime; 
    char m_pad88_6912[88];
    int32 m_iNumEmptyAttacks; // Size: 92
    GameTime_t m_flLastMagDropRequestTime; 
    float32 m_flWatTickOffset; 
};

struct __declspec(align(16))  C_CSWeaponBaseGun {
    char m_pad[6928];
    int32 m_zoomLevel; 
    int32 m_iBurstShotsRemaining; 
    char m_pad12_6952[12];
    int32 m_iSilencerBodygroup; // Size: 16
    int32 m_silencedModelIndex; 
    bool m_inPrecache; 
    bool m_bNeedsBoltAction; 
};

struct __declspec(align(16))  C_C4 {
    char m_pad[6928];
    char[32] m_szScreenText; // Size: 32
    ParticleIndex_t m_activeLightParticleIndex; 
    C4LightEffect_t m_eActiveLightEffect; 
    char m_pad3_6972[3];
    bool m_bStartedArming; 
    GameTime_t m_fArmedTime; 
    bool m_bBombPlacedAnimation; 
    char m_pad6_6984[6];
    bool m_bIsPlantingViaUse; 
    EntitySpottedState_t m_entitySpottedState; // Size: 24
    int32 m_nSpotRules; 
    bool[7] m_bPlayedArmingBeeps; 
    bool m_bBombPlanted; 
};

struct __declspec(align(16))  C_DEagle {
};

struct __declspec(align(16))  C_WeaponElite {
};

struct __declspec(align(16))  C_WeaponNOVA {
};

struct __declspec(align(16))  C_WeaponSawedoff {
};

struct __declspec(align(16))  C_WeaponTaser {
    char m_pad[6960];
    GameTime_t m_fFireTime; 
    int32 m_nLastAttackTick; 
};

struct __declspec(align(16))  C_WeaponXM1014 {
};

struct __declspec(align(16))  C_Knife {
};

struct __declspec(align(16))  C_Melee {
};

struct __declspec(align(16))  C_WeaponShield {
    char m_pad[6960];
    float32 m_flDisplayHealth; 
};

struct __declspec(align(8))  C_MolotovProjectile {
    char m_pad[4616];
    bool m_bIsIncGrenade; 
};

struct __declspec(align(8))  C_DecoyProjectile {
    char m_pad[4616];
    int32 m_nDecoyShotTick; 
    char m_pad32_4656[32];
    int32 m_nClientLastKnownDecoyShotTick; // Size: 36
    GameTime_t m_flTimeParticleEffectSpawn; 
};

struct __declspec(align(8))  C_SmokeGrenadeProjectile {
    char m_pad[4624];
    int32 m_nSmokeEffectTickBegin; 
    char m_pad3_4632[3];
    bool m_bDidSmokeEffect; 
    int32 m_nRandomSeed; 
    Vector m_vSmokeColor; // Size: 12
    Vector m_vSmokeDetonationPos; // Size: 16
    CUtlVector< uint8 > m_VoxelFrameData; // Size: 24
    bool m_bSmokeVolumeDataReceived; 
    bool m_bSmokeEffectSpawned; 
};

struct  C_BaseCSGrenade {
    char m_pad[6928];
    bool m_bClientPredictDelete; 
    bool m_bRedraw; 
    bool m_bIsHeldByPlayer; 
    bool m_bPinPulled; 
    bool m_bJumpThrow; 
    char m_pad2_6936[2];
    bool m_bThrowAnimating; 
    GameTime_t m_fThrowTime; 
    float32 m_flThrowStrength; 
    float32 m_flThrowStrengthApproach; 
    GameTime_t m_fDropTime; 
    GameTime_t m_fPinPullTime; 
    char m_pad3_6960[3];
    bool m_bJustPulledPin; 
    GameTick_t m_nNextHoldTick; 
    float32 m_flNextHoldFrac; 
    CHandle< C_CSWeaponBase > m_hSwitchToWeaponAfterThrow; 
};

struct  C_WeaponBaseItem {
    char m_pad[6928];
    CountdownTimer m_SequenceCompleteTimer; // Size: 24
    bool m_bRedraw; 
};

struct __declspec(align(8))  C_ItemDogtags {
    char m_pad[5992];
    CHandle< C_CSPlayerPawn > m_OwningPlayer; 
    CHandle< C_CSPlayerPawn > m_KillingPlayer; 
};

struct __declspec(align(16))  C_Item_Healthshot {
};

struct __declspec(align(16))  C_Fists {
    char m_pad[6928];
    char m_pad3_6932[3];
    bool m_bPlayingUninterruptableAct; 
    PlayerAnimEvent_t m_nUninterruptableActivity; 
};

struct __declspec(align(16))  C_SensorGrenade {
};

struct __declspec(align(16))  CBreachCharge {
};

struct __declspec(align(16))  CBumpMine {
};

struct __declspec(align(16))  CTablet {
};

struct __declspec(align(16))  CTripWireFire {
};

struct __declspec(align(16))  CWeaponZoneRepulsor {
};

struct __declspec(align(8))  C_CSPlayerPawnBase {
    char m_pad[4960];
    CCSPlayer_PingServices* m_pPingServices; // Size: 8
    CPlayer_ViewModelServices* m_pViewModelServices; // Size: 8
    float32[4] m_fRenderingClipPlane; // Size: 16
    int32 m_nLastClipPlaneSetupFrame; 
    Vector m_vecLastClipCameraPos; // Size: 12
    Vector m_vecLastClipCameraForward; // Size: 12
    bool m_bClipHitStaticWorld; 
    char m_pad2_5024[2];
    bool m_bCachedPlaneIsValid; 
    C_CSWeaponBase* m_pClippingWeapon; // Size: 8
    CSPlayerState m_previousPlayerState; 
    CSPlayerState m_iPlayerState; 
    char m_pad3_5044[3];
    bool m_bIsRescuing; 
    GameTime_t m_fImmuneToGunGameDamageTime; 
    GameTime_t m_fImmuneToGunGameDamageTimeLast; 
    bool m_bGunGameImmunity; 
    char m_pad2_5056[2];
    bool m_bHasMovedSinceSpawn; 
    float32 m_fMolotovUseTime; 
    float32 m_fMolotovDamageTime; 
    int32 m_iThrowGrenadeCounter; 
    GameTime_t m_flLastSpawnTimeIndex; 
    int32 m_iProgressBarDuration; 
    float32 m_flProgressBarStartTime; 
    Vector m_vecIntroStartEyePosition; // Size: 12
    Vector m_vecIntroStartPlayerForward; // Size: 12
    GameTime_t m_flClientDeathTime; 
    char m_pad3_5112[3];
    bool m_bScreenTearFrameCaptured; 
    float32 m_flFlashBangTime; 
    float32 m_flFlashScreenshotAlpha; 
    float32 m_flFlashOverlayAlpha; 
    bool m_bFlashBuildUp; 
    bool m_bFlashDspHasBeenCleared; 
    char m_pad1_5128[1];
    bool m_bFlashScreenshotHasBeenGrabbed; 
    float32 m_flFlashMaxAlpha; 
    float32 m_flFlashDuration; 
    int32 m_iHealthBarRenderMaskIndex; 
    float32 m_flHealthFadeValue; 
    char m_pad12_5160[12];
    float32 m_flHealthFadeAlpha; // Size: 16
    float32 m_flDeathCCWeight; 
    float32 m_flPrevRoundEndTime; 
    char m_pad4_5176[4];
    float32 m_flPrevMatchEndTime; // Size: 8
    QAngle m_angEyeAngles; // Size: 24
    float32 m_fNextThinkPushAway; 
    bool m_bShouldAutobuyDMWeapons; 
    char m_pad2_5208[2];
    bool m_bShouldAutobuyNow; 
    CEntityIndex m_iIDEntIndex; // Size: 8
    CountdownTimer m_delayTargetIDTimer; // Size: 24
    CEntityIndex m_iTargetItemEntIdx; 
    CEntityIndex m_iOldIDEntIndex; 
    CountdownTimer m_holdTargetIDTimer; // Size: 28
    float32 m_flCurrentMusicStartTime; 
    float32 m_flMusicRoundStartTime; 
    char m_pad3_5288[3];
    bool m_bDeferStartMusicOnWarmup; 
    int32 m_cycleLatch; 
    float32 m_serverIntendedCycle; 
    float32 m_flLastSmokeOverlayAlpha; 
    float32 m_flLastSmokeAge; 
    Vector m_vLastSmokeOverlayColor; // Size: 12
    ParticleIndex_t m_nPlayerSmokedFx; 
    ParticleIndex_t m_nPlayerInfernoBodyFx; 
    ParticleIndex_t m_nPlayerInfernoFootFx; 
    float32 m_flNextMagDropTime; 
    int32 m_nLastMagDropAttachmentIndex; 
    Vector m_vecLastAliveLocalVelocity; // Size: 40
    char m_pad7_5384[7];
    bool m_bGuardianShouldSprayCustomXMark; // Size: 8
    CHandle< CCSPlayerController > m_hOriginalController; 
};

struct __declspec(align(8))  C_Hostage {
    char m_pad[4520];
    EntitySpottedState_t m_entitySpottedState; // Size: 24
    CHandle< C_BaseEntity > m_leader; // Size: 8
    CountdownTimer m_reuseTimer; // Size: 24
    Vector m_vel; // Size: 12
    bool m_isRescued; 
    char m_pad2_4592[2];
    bool m_jumpedThisFrame; 
    int32 m_nHostageState; 
    char m_pad3_4600[3];
    bool m_bHandsHaveBeenCut; 
    CHandle< C_CSPlayerPawn > m_hHostageGrabber; 
    GameTime_t m_fLastGrabTime; 
    Vector m_vecGrabbedPos; // Size: 12
    GameTime_t m_flRescueStartTime; 
    GameTime_t m_flGrabSuccessTime; 
    GameTime_t m_flDropStartTime; 
    GameTime_t m_flDeadOrRescuedTime; // Size: 8
    CountdownTimer m_blinkTimer; // Size: 24
    Vector m_lookAt; // Size: 16
    CountdownTimer m_lookAroundTimer; // Size: 24
    bool m_isInit; 
    AttachmentHandle_t m_eyeAttachment; 
    AttachmentHandle_t m_chestAttachment; 
    CBasePlayerController* m_pPredictionOwner; // Size: 8
    GameTime_t m_fNewestAlphaThinkTime; 
};

struct __declspec(align(8))  C_NetTestBaseCombatCharacter {
};

struct __declspec(align(16))  C_AK47 {
};

struct __declspec(align(16))  C_WeaponAug {
};

struct __declspec(align(16))  C_WeaponAWP {
};

struct __declspec(align(16))  C_WeaponBizon {
};

struct __declspec(align(16))  C_WeaponFamas {
};

struct __declspec(align(16))  C_WeaponFiveSeven {
};

struct __declspec(align(16))  C_WeaponG3SG1 {
};

struct __declspec(align(16))  C_WeaponGalilAR {
};

struct __declspec(align(16))  C_WeaponGlock {
};

struct __declspec(align(16))  C_WeaponHKP2000 {
};

struct __declspec(align(16))  C_WeaponUSPSilencer {
};

struct __declspec(align(16))  C_WeaponM4A1 {
};

struct __declspec(align(16))  C_WeaponM4A1Silencer {
};

struct __declspec(align(16))  C_WeaponMAC10 {
};

struct __declspec(align(16))  C_WeaponMag7 {
};

struct __declspec(align(16))  C_WeaponMP5SD {
};

struct __declspec(align(16))  C_WeaponMP7 {
};

struct __declspec(align(16))  C_WeaponMP9 {
};

struct __declspec(align(16))  C_WeaponNegev {
};

struct __declspec(align(16))  C_WeaponP250 {
};

struct __declspec(align(16))  C_WeaponCZ75a {
};

struct __declspec(align(16))  C_WeaponP90 {
};

struct __declspec(align(16))  C_WeaponSCAR20 {
};

struct __declspec(align(16))  C_WeaponSG556 {
};

struct __declspec(align(16))  C_WeaponSSG08 {
};

struct __declspec(align(16))  C_WeaponTec9 {
};

struct __declspec(align(16))  C_WeaponUMP45 {
};

struct __declspec(align(16))  C_WeaponM249 {
};

struct __declspec(align(16))  C_WeaponRevolver {
};

struct __declspec(align(16))  C_MolotovGrenade {
};

struct __declspec(align(16))  C_IncendiaryGrenade {
};

struct __declspec(align(16))  C_DecoyGrenade {
};

struct __declspec(align(16))  C_Flashbang {
};

struct __declspec(align(16))  C_HEGrenade {
};

struct __declspec(align(16))  C_SmokeGrenade {
};

struct __declspec(align(16))  C_CSGO_PreviewPlayer {
    char m_pad[14896];
    CUtlString m_animgraph; // Size: 8
    CGlobalSymbol m_animgraphCharacterModeString; // Size: 8
    float32 m_flInitialModelScale; 
};

struct __declspec(align(16))  C_CSGO_PreviewPlayerAlias_csgo_player_previewmodel {
};


```
