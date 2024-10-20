# cs2classes
my discord: patekfr

struct CScriptComponent {
    char m_pad[48];
    CUtlSymbolLarge m_scriptClassName;
};

struct __declspec(align(8)) C_BaseEntity {
    char m_pad[56];
    CBodyComponent* m_CBodyComponent;
    CNetworkTransmitComponent m_NetworkTransmitComponent;
    GameTick_t m_nLastThinkTick;
    CGameSceneNode* m_pGameSceneNode;
    CRenderComponent* m_pRenderComponent;
    CCollisionProperty* m_pCollision;
    int32 m_iMaxHealth;
    int32 m_iHealth;
    uint8 m_lifeState;
    bool m_bTakesDamage;
    TakeDamageFlags_t m_nTakeDamageFlags;
    EntityPlatformTypes_t m_nPlatformType;
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
    CUtlStringToken m_nSubclassID;
    int32 m_nSimulationTick;
    int32 m_iCurrentThinkContext;
    CUtlVector< thinkfunc_t > m_aThinkFunctions;
    bool m_bDisabledContextThinks;
    float32 m_flAnimTime;
    float32 m_flSimulationTime;
    uint8 m_nSceneObjectOverrideFlags;
    bool m_bHasSuccessfullyInterpolated;
    bool m_bHasAddedVarsToInterpolation;
    bool m_bRenderEvenWhenNotSuccessfullyInterpolated;
    int32[2] m_nInterpolationLatchDirtyFlags;
    uint16[11] m_ListEntry;
    GameTime_t m_flCreateTime;
    float32 m_flSpeed;
    uint16 m_EntClientFlags;
    bool m_bClientSideRagdoll;
    uint8 m_iTeamNum;
    uint32 m_spawnflags;
    GameTick_t m_nNextThinkTick;
    uint32 m_fFlags;
    Vector m_vecAbsVelocity;
    CNetworkVelocityVector m_vecVelocity;
    Vector m_vecBaseVelocity;
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
    bool m_bAnimatedEveryTick;
    GameTime_t m_flNavIgnoreUntilTime;
    uint16 m_hThink;
    uint8 m_fBBoxVisFlags;
    bool m_bPredictable;
    bool m_bRenderWithViewModels;
    CSplitScreenSlot m_nSplitUserPlayerPredictionSlot;
    int32 m_nFirstPredictableCommand;
    int32 m_nLastPredictableCommand;
    CHandle< C_BaseEntity > m_hOldMoveParent;
    CParticleProperty m_Particles;
    CUtlVector< float32 > m_vecPredictedScriptFloats;
    CUtlVector< int32 > m_vecPredictedScriptFloatIDs;
    int32 m_nNextScriptVarRecordID;
    QAngle m_vecAngVelocity;
    int32 m_DataChangeEventRef;
    CUtlVector< CEntityHandle > m_dependencies;
    int32 m_nCreationTick;
    bool m_bAnimTimeChanged;
    bool m_bSimulationTimeChanged;
    CUtlString m_sUniqueHammerID;
    BloodType m_nBloodType;
};

struct CountdownTimer {
    char m_pad[8];
    float32 m_duration;
    GameTime_t m_timestamp;
    float32 m_timescale;
    WorldGroupId_t m_nWorldGroupId;
};

struct CEntityComponent {
};

struct CEntityIdentity {
    char m_pad[20];
    int32 m_nameStringableIndex;
    CUtlSymbolLarge m_name;
    CUtlSymbolLarge m_designerName;
    uint32 m_flags;
    WorldGroupId_t m_worldGroupId;
    uint32 m_fDataObjectTypes;
    ChangeAccessorFieldPathIndex_t m_PathIndex;
    CEntityIdentity* m_pPrev;
    CEntityIdentity* m_pNext;
    CEntityIdentity* m_pPrevByClass;
    CEntityIdentity* m_pNextByClass;
};

struct CEntityInstance {
    char m_pad[8];
    CUtlSymbolLarge m_iszPrivateVScripts;
    CEntityIdentity* m_pEntity;
    CScriptComponent* m_CScriptComponent;
    bool m_bVisibleinPVS;
};

struct CGameSceneNode {
    char m_pad[16];
    CTransform m_nodeToWorld;
    CEntityInstance* m_pOwner;
    CGameSceneNode* m_pParent;
    CGameSceneNode* m_pChild;
    CGameSceneNode* m_pNextSibling;
    CGameSceneNodeHandle m_hParent;
    CNetworkOriginCellCoordQuantizedVector m_vecOrigin;
    QAngle m_angRotation;
    float32 m_flScale;
    Vector m_vecAbsOrigin;
    QAngle m_angAbsRotation;
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
    bitfield:1 m_bDirtyBoneMergeBoneToRoot;
    uint8 m_nHierarchicalDepth;
    uint8 m_nHierarchyType;
    uint8 m_nDoNotSetAnimTimeInInvalidatePhysicsCount;
    CUtlStringToken m_name;
    CUtlStringToken m_hierarchyAttachName;
    float32 m_flZOffset;
    float32 m_flClientLocalScale;
    Vector m_vRenderOrigin;
};

struct CBodyComponent {
    char m_pad[8];
    CGameSceneNode* m_pSceneNode;
    CNetworkVarChainer __m_pChainEntity;
};

struct CBodyComponentPoint {
    char m_pad[80];
    CGameSceneNode m_sceneNode;
};

struct CSkeletonInstance {
    char m_pad[368];
    CModelState m_modelState;
    bool m_bIsAnimationEnabled;
    bool m_bUseParentRenderBounds;
    bool m_bDisableSolidCollisionsForHierarchy;
    bitfield:1 m_bDirtyMotionType;
    bitfield:1 m_bIsGeneratingLatchedParentSpaceState;
    CUtlStringToken m_materialGroup;
    uint8 m_nHitboxSet;
};

struct CBodyComponentSkeletonInstance {
    char m_pad[80];
    CSkeletonInstance m_skeletonInstance;
};

struct CHitboxComponent {
    char m_pad[36];
    uint32[1] m_bvDisabledHitGroups;
};

struct CLightComponent {
    char m_pad[56];
    CNetworkVarChainer __m_pChainEntity;
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
    CStrongHandle< InfoForResourceTypeCTextureBase > m_hLightCookie;
    int32 m_nCascades;
    int32 m_nCastShadows;
    int32 m_nShadowWidth;
    int32 m_nShadowHeight;
    bool m_bRenderDiffuse;
    int32 m_nRenderSpecular;
    bool m_bRenderTransmissive;
    float32 m_flOrthoLightWidth;
    float32 m_flOrthoLightHeight;
    int32 m_nStyle;
    CUtlString m_Pattern;
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
    bool m_bUsesBakedShadowing;
    int32 m_nShadowPriority;
    int32 m_nBakedShadowIndex;
    bool m_bRenderToCubemaps;
    int32 m_nDirectLight;
    int32 m_nIndirectLight;
    float32 m_flFadeMinDist;
    float32 m_flFadeMaxDist;
    float32 m_flShadowFadeMinDist;
    float32 m_flShadowFadeMaxDist;
    bool m_bEnabled;
    bool m_bFlicker;
    bool m_bPrecomputedFieldsValid;
    Vector m_vPrecomputedBoundsMins;
    Vector m_vPrecomputedBoundsMaxs;
    Vector m_vPrecomputedOBBOrigin;
    QAngle m_vPrecomputedOBBAngles;
    Vector m_vPrecomputedOBBExtent;
    float32 m_flPrecomputedMaxRange;
    int32 m_nFogLightingMode;
    float32 m_flFogContributionStength;
    float32 m_flNearClipPlane;
    Color m_SkyColor;
    float32 m_flSkyIntensity;
    Color m_SkyAmbientBounce;
    bool m_bUseSecondaryColor;
    bool m_bMixedShadows;
    GameTime_t m_flLightStyleStartTime;
    float32 m_flCapsuleLength;
    float32 m_flMinRoughness;
};

struct CRenderComponent {
    char m_pad[16];
    CNetworkVarChainer __m_pChainEntity;
    bool m_bIsRenderingWithViewModels;
    uint32 m_nSplitscreenFlags;
    bool m_bEnableRendering;
    bool m_bInterpolationReadyToDraw;
};

struct __declspec(align(8)) C_PointCamera {
    char m_pad[1384];
    float32 m_FOV;
    float32 m_Resolution;
    bool m_bFogEnable;
    Color m_FogColor;
    float32 m_flFogStart;
    float32 m_flFogEnd;
    float32 m_flFogMaxDensity;
    bool m_bActive;
    bool m_bUseScreenAspectRatio;
    float32 m_flAspectRatio;
    bool m_bNoSky;
    float32 m_fBrightness;
    float32 m_flZFar;
    float32 m_flZNear;
    bool m_bCanHLTVUse;
    bool m_bAlignWithParent;
    bool m_bDofEnabled;
    float32 m_flDofNearBlurry;
    float32 m_flDofNearCrisp;
    float32 m_flDofFarCrisp;
    float32 m_flDofFarBlurry;
    float32 m_flDofTiltToGround;
    float32 m_TargetFOV;
    float32 m_DegreesPerSecond;
    bool m_bIsOn;
    C_PointCamera* m_pNext;
};

struct CPointTemplateAPI {
};

struct CPropDataComponent {
    char m_pad[16];
    float32 m_flDmgModBullet;
    float32 m_flDmgModClub;
    float32 m_flDmgModExplosive;
    float32 m_flDmgModFire;
    CUtlSymbolLarge m_iszPhysicsDamageTableName;
    CUtlSymbolLarge m_iszBasePropData;
    int32 m_nInteractions;
    bool m_bSpawnMotionDisabled;
    int32 m_nDisableTakePhysicsDamageSpawnFlag;
    int32 m_nMotionDisabledSpawnFlag;
};

struct CBuoyancyHelper {
    char m_pad[24];
    CUtlStringToken m_nFluidType;
    float32 m_flFluidDensity;
    CUtlVector< float32 > m_vecFractionOfWheelSubmergedForWheelFriction;
    CUtlVector< float32 > m_vecWheelFrictionScales;
    CUtlVector< float32 > m_vecFractionOfWheelSubmergedForWheelDrag;
    CUtlVector< float32 > m_vecWheelDrag;
};

struct __declspec(align(8)) CBaseAnimGraph {
    char m_pad[3488];
    bool m_bInitiallyPopulateInterpHistory;
    bool m_bSuppressAnimEventSounds;
    bool m_bAnimGraphUpdateEnabled;
    float32 m_flMaxSlopeDistance;
    Vector m_vLastSlopeCheckPos;
    bool m_bAnimationUpdateScheduled;
    Vector m_vecForce;
    int32 m_nForceBone;
    CBaseAnimGraph* m_pClientsideRagdoll;
    bool m_bBuiltRagdoll;
    PhysicsRagdollPose_t m_RagdollPose;
    bool m_bRagdollClientSide;
    bool m_bHasAnimatedMaterialAttributes;
};

struct CSharedGapTypeQueryRegistration {
};

struct CBasePlayerControllerAPI {
};

struct C_CommandContext {
    char m_pad[0];
    bool needsprocessing;
    int32 command_number;
};

struct ViewAngleServerChange_t {
    char m_pad[48];
    FixAngleSet_t nType;
    QAngle qAngle;
    uint32 nIndex;
};

struct CPlayer_AutoaimServices {
};

struct audioparams_t {
    char m_pad[8];
    Vector[8] localSound;
    int32 soundscapeIndex;
    uint8 localBits;
    int32 soundscapeEntityListIndex;
    uint32 soundEventHash;
};

struct C_fogplayerparams_t {
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

struct __declspec(align(8)) C_ColorCorrection {
    char m_pad[1384];
    Vector m_vecOrigin;
    float32 m_MinFalloff;
    float32 m_MaxFalloff;
    float32 m_flFadeInDuration;
    float32 m_flFadeOutDuration;
    float32 m_flMaxWeight;
    float32 m_flCurWeight;
    char[512] m_netlookupFilename;
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

struct __declspec(align(8)) C_TonemapController2 {
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

struct __declspec(align(8)) C_PostProcessingVolume {
    char m_pad[3392];
    CStrongHandle< InfoForResourceTypeCPostProcessingResource > m_hPostSettings;
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
    bool m_bExposureControl;
    float32 m_flRate;
    float32 m_flTonemapPercentTarget;
    float32 m_flTonemapPercentBrightPixels;
    float32 m_flTonemapMinAvgLum;
};

struct fogparams_t {
    char m_pad[8];
    Vector dirPrimary;
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

struct __declspec(align(8)) C_FogController {
    char m_pad[1384];
    fogparams_t m_fog;
    bool m_bUseAngles;
    int32 m_iChangedVariables;
};

struct CPlayer_CameraServices {
    char m_pad[64];
    QAngle m_vecCsViewPunchAngle;
    GameTick_t m_nCsViewPunchAngleTick;
    float32 m_flCsViewPunchAngleTickRatio;
    C_fogplayerparams_t m_PlayerFog;
    CHandle< C_ColorCorrection > m_hColorCorrectionCtrl;
    CHandle< C_BaseEntity > m_hViewEntity;
    CHandle< C_TonemapController2 > m_hTonemapController;
    audioparams_t m_audio;
    C_NetworkUtlVectorBase< CHandle< C_PostProcessingVolume > > m_PostProcessingVolumes;
    float32 m_flOldPlayerZ;
    float32 m_flOldPlayerViewOffsetZ;
    fogparams_t m_CurrentFog;
    CHandle< C_FogController > m_hOldFogController;
    bool[5] m_bOverrideFogColor;
    Color[5] m_OverrideFogColor;
    bool[5] m_bOverrideFogStartEnd;
    float32[5] m_fOverrideFogStart;
    float32[5] m_fOverrideFogEnd;
    CHandle< C_PostProcessingVolume > m_hActivePostProcessingVolume;
    QAngle m_angDemoViewAngles;
};

struct CPlayer_FlashlightServices {
};

struct CPlayer_ItemServices {
};

struct CPlayer_MovementServices {
    char m_pad[64];
    int32 m_nImpulse;
    CInButtonState m_nButtons;
    uint64 m_nQueuedButtonDownMask;
    uint64 m_nQueuedButtonChangeMask;
    uint64 m_nButtonDoublePressed;
    uint32[64] m_pButtonPressedCmdNumber;
    uint32 m_nLastCommandNumberProcessed;
    uint64 m_nToggleButtonDownMask;
    float32 m_flMaxspeed;
    float32[4] m_arrForceSubtickMoveWhen;
    float32 m_flForwardMove;
    float32 m_flLeftMove;
    float32 m_flUpMove;
    Vector m_vecLastMovementImpulses;
    QAngle m_vecOldViewAngles;
};

struct CPlayer_MovementServices_Humanoid {
    char m_pad[472];
    float32 m_flStepSoundTime;
    float32 m_flFallVelocity;
    bool m_bInCrouch;
    uint32 m_nCrouchState;
    GameTime_t m_flCrouchTransitionStartTime;
    bool m_bDucked;
    bool m_bDucking;
    bool m_bInDuckJump;
    Vector m_groundNormal;
    float32 m_flSurfaceFriction;
    CUtlStringToken m_surfaceProps;
    int32 m_nStepside;
};

struct CPlayer_ObserverServices {
    char m_pad[64];
    uint8 m_iObserverMode;
    CHandle< C_BaseEntity > m_hObserverTarget;
    ObserverMode_t m_iObserverLastMode;
    bool m_bForcedObserverMode;
    float32 m_flObserverChaseDistance;
    GameTime_t m_flObserverChaseDistanceCalcTime;
};

struct CPlayer_UseServices {
};

struct CPlayer_WaterServices {
};

struct __declspec(align(8)) C_BasePlayerWeapon {
    char m_pad[5736];
    GameTick_t m_nNextPrimaryAttackTick;
    float32 m_flNextPrimaryAttackTickRatio;
    GameTick_t m_nNextSecondaryAttackTick;
    float32 m_flNextSecondaryAttackTickRatio;
    int32 m_iClip1;
    int32 m_iClip2;
    int32[2] m_pReserveAmmo;
};

struct CPlayer_WeaponServices {
    char m_pad[64];
    C_NetworkUtlVectorBase< CHandle< C_BasePlayerWeapon > > m_hMyWeapons;
    CHandle< C_BasePlayerWeapon > m_hActiveWeapon;
    CHandle< C_BasePlayerWeapon > m_hLastWeapon;
    uint16[32] m_iAmmo;
};

struct CBaseAnimGraphController {
    char m_pad[24];
    CAnimGraphNetworkedVariables m_animGraphNetworkedVars;
    bool m_bSequenceFinished;
    float32 m_flSoundSyncTime;
    uint32 m_nActiveIKChainMask;
    HSequence m_hSequence;
    GameTime_t m_flSeqStartTime;
    float32 m_flSeqFixedCycle;
    AnimLoopMode_t m_nAnimLoopMode;
    CNetworkedQuantizedFloat m_flPlaybackRate;
    SequenceFinishNotifyState_t m_nNotifyState;
    bool m_bNetworkedAnimationInputsChanged;
    bool m_bNetworkedSequenceChanged;
    bool m_bLastUpdateSkipped;
    GameTime_t m_flPrevAnimUpdateTime;
};

struct CBodyComponentBaseAnimGraph {
    char m_pad[1168];
    CBaseAnimGraphController m_animationController;
};

struct EntityRenderAttribute_t {
    char m_pad[48];
    CUtlStringToken m_ID;
    Vector4D m_Values;
};

struct __declspec(align(8)) C_BaseModelEntity {
    char m_pad[2640];
    CRenderComponent* m_CRenderComponent;
    CHitboxComponent m_CHitboxComponent;
    HitGroup_t m_LastHitGroup;
    bool m_bInitModelEffects;
    bool m_bIsStaticProp;
    int32 m_nLastAddDecal;
    int32 m_nDecalsAdded;
    int32 m_iOldHealth;
    RenderMode_t m_nRenderMode;
    RenderFx_t m_nRenderFX;
    bool m_bAllowFadeInView;
    Color m_clrRender;
    C_UtlVectorEmbeddedNetworkVar< EntityRenderAttribute_t > m_vecRenderAttributes;
    bool m_bRenderToCubemaps;
    bool m_bNoInterpolate;
    CCollisionProperty m_Collision;
    CGlowProperty m_Glow;
    float32 m_flGlowBackfaceMult;
    float32 m_fadeMinDist;
    float32 m_fadeMaxDist;
    float32 m_flFadeScale;
    float32 m_flShadowStrength;
    uint8 m_nObjectCulling;
    int32 m_nAddDecal;
    Vector m_vDecalPosition;
    Vector m_vDecalForwardAxis;
    float32 m_flDecalHealBloodRate;
    float32 m_flDecalHealHeightRate;
    C_NetworkUtlVectorBase< CHandle< C_BaseModelEntity > > m_ConfigEntitiesToPropagateMaterialDecalsTo;
    CNetworkViewOffsetVector m_vecViewOffset;
    CClientAlphaProperty* m_pClientAlphaProperty;
    Color m_ClientOverrideTint;
    bool m_bUseClientOverrideTint;
};

struct ActiveModelConfig_t {
    char m_pad[40];
    ModelConfigHandle_t m_Handle;
    CUtlSymbolLarge m_Name;
    C_NetworkUtlVectorBase< CHandle< C_BaseModelEntity > > m_AssociatedEntities;
    C_NetworkUtlVectorBase< CUtlSymbolLarge > m_AssociatedEntityNames;
};

struct CBodyComponentBaseModelEntity {
};

struct CGameSceneNodeHandle {
    char m_pad[8];
    CEntityHandle m_hOwner;
    CUtlStringToken m_name;
};

struct CPathSimpleAPI {
};

struct SequenceHistory_t {
    char m_pad[0];
    HSequence m_hSequence;
    GameTime_t m_flSeqStartTime;
    float32 m_flSeqFixedCycle;
    AnimLoopMode_t m_nSeqLoopMode;
    float32 m_flPlaybackRate;
    float32 m_flCyclesPerSecond;
};

struct CNetworkedSequenceOperation {
    char m_pad[8];
    HSequence m_hSequence;
    float32 m_flPrevCycle;
    float32 m_flCycle;
    CNetworkedQuantizedFloat m_flWeight;
    bool m_bSequenceChangeNetworked;
    bool m_bDiscontinuity;
    float32 m_flPrevCycleFromDiscontinuity;
    float32 m_flPrevCycleForAnimEventDetection;
};

struct CModelState {
    char m_pad[160];
    CStrongHandle< InfoForResourceTypeCModel > m_hModel;
    CUtlSymbolLarge m_ModelName;
    bool m_bClientClothCreationSuppressed;
    uint64 m_MeshGroupMask;
    int8 m_nIdealMotionType;
    int8 m_nForceLOD;
    int8 m_nClothUpdateFlags;
};

struct IntervalTimer {
    char m_pad[8];
    GameTime_t m_timestamp;
    WorldGroupId_t m_nWorldGroupId;
};

struct EngineCountdownTimer {
    char m_pad[8];
    float32 m_duration;
    float32 m_timestamp;
    float32 m_timescale;
};

struct CTimeline {
    char m_pad[16];
    float32[64] m_flValues;
    int32[64] m_nValueCounts;
    int32 m_nBucketCount;
    float32 m_flInterval;
    float32 m_flFinalValue;
    TimelineCompression_t m_nCompressionType;
    bool m_bStopped;
};

struct CAnimGraphNetworkedVariables {
    char m_pad[8];
    C_NetworkUtlVectorBase< uint32 > m_PredNetBoolVariables;
    C_NetworkUtlVectorBase< uint8 > m_PredNetByteVariables;
    C_NetworkUtlVectorBase< uint16 > m_PredNetUInt16Variables;
    C_NetworkUtlVectorBase< int32 > m_PredNetIntVariables;
    C_NetworkUtlVectorBase< uint32 > m_PredNetUInt32Variables;
    C_NetworkUtlVectorBase< uint64 > m_PredNetUInt64Variables;
    C_NetworkUtlVectorBase< float32 > m_PredNetFloatVariables;
    C_NetworkUtlVectorBase< Vector > m_PredNetVectorVariables;
    C_NetworkUtlVectorBase< Quaternion > m_PredNetQuaternionVariables;
    C_NetworkUtlVectorBase< CGlobalSymbol > m_PredNetGlobalSymbolVariables;
    C_NetworkUtlVectorBase< uint32 > m_OwnerOnlyPredNetBoolVariables;
    C_NetworkUtlVectorBase< uint8 > m_OwnerOnlyPredNetByteVariables;
    C_NetworkUtlVectorBase< uint16 > m_OwnerOnlyPredNetUInt16Variables;
    C_NetworkUtlVectorBase< int32 > m_OwnerOnlyPredNetIntVariables;
    C_NetworkUtlVectorBase< uint32 > m_OwnerOnlyPredNetUInt32Variables;
    C_NetworkUtlVectorBase< uint64 > m_OwnerOnlyPredNetUInt64Variables;
    C_NetworkUtlVectorBase< float32 > m_OwnerOnlyPredNetFloatVariables;
    C_NetworkUtlVectorBase< Vector > m_OwnerOnlyPredNetVectorVariables;
    C_NetworkUtlVectorBase< Quaternion > m_OwnerOnlyPredNetQuaternionVariables;
    C_NetworkUtlVectorBase< CGlobalSymbol > m_OwnerOnlyPredNetGlobalSymbolVariables;
    int32 m_nBoolVariablesCount;
    int32 m_nOwnerOnlyBoolVariablesCount;
    int32 m_nRandomSeedOffset;
    float32 m_flLastTeleportTime;
};

struct C_BaseEntityAPI {
};

struct CTakeDamageInfoAPI {
};

struct CClientGapTypeQueryRegistration {
};

struct CCollisionProperty {
    char m_pad[16];
    VPhysicsCollisionAttribute_t m_collisionAttribute;
    Vector m_vecMins;
    Vector m_vecMaxs;
    uint8 m_usSolidFlags;
    SolidType_t m_nSolidType;
    uint8 m_triggerBloat;
    SurroundingBoundsType_t m_nSurroundType;
    uint8 m_CollisionGroup;
    uint8 m_nEnablePhysics;
    float32 m_flBoundingRadius;
    Vector m_vecSpecifiedSurroundingMins;
    Vector m_vecSpecifiedSurroundingMaxs;
    Vector m_vecSurroundingMaxs;
    Vector m_vecSurroundingMins;
    Vector m_vCapsuleCenter1;
    Vector m_vCapsuleCenter2;
    float32 m_flCapsuleRadius;
};

struct __declspec(align(8)) CBasePlayerController {
    char m_pad[1392];
    int32 m_nFinalPredictedTick;
    C_CommandContext m_CommandContext;
    uint64 m_nInButtonsWhichAreToggles;
    uint32 m_nTickBase;
    CHandle< C_BasePlayerPawn > m_hPawn;
    bool m_bKnownTeamMismatch;
    CHandle< C_BasePlayerPawn > m_hPredictedPawn;
    CSplitScreenSlot m_nSplitScreenSlot;
    CHandle< CBasePlayerController > m_hSplitOwner;
    CUtlVector< CHandle< CBasePlayerController > > m_hSplitScreenPlayers;
    bool m_bIsHLTV;
    PlayerConnectedState m_iConnected;
    char[128] m_iszPlayerName;
    uint64 m_steamID;
    bool m_bIsLocalPlayerController;
    uint32 m_iDesiredFOV;
};

struct __declspec(align(8)) CLogicalEntity {
};

struct C_BaseFlex::Emphasized_Phoneme {
    char m_pad[0];
    CUtlString m_sClassName;
    float32 m_flAmount;
    bool m_bRequired;
    bool m_bBasechecked;
    bool m_bValid;
};

struct C_EnvWindShared {
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
    uint16 m_iGustDirChange;
    Vector m_location;
    int32 m_iszGustSound;
    int32 m_iWindDir;
    float32 m_flWindSpeed;
    Vector m_currentWindVector;
    Vector m_CurrentSwayVector;
    Vector m_PrevSwayVector;
    uint16 m_iInitialWindDir;
    float32 m_flInitialWindSpeed;
    GameTime_t m_flVariationTime;
    GameTime_t m_flSwayTime;
    GameTime_t m_flSimTime;
    GameTime_t m_flSwitchTime;
    float32 m_flAveWindSpeed;
    bool m_bGusting;
    float32 m_flWindAngleVariation;
    float32 m_flWindSpeedVariation;
    CHandle< C_BaseEntity > m_hEntOwner;
};

struct __declspec(align(8)) C_EnvWindClientside {
    char m_pad[1384];
    C_EnvWindShared m_EnvWindShared;
};

struct __declspec(align(8)) C_EntityFlame {
    char m_pad[1384];
    CHandle< C_BaseEntity > m_hEntAttached;
    CHandle< C_BaseEntity > m_hOldAttached;
    bool m_bCheapEffect;
};

struct CProjectedTextureBase {
    char m_pad[12];
    CHandle< C_BaseEntity > m_hTargetEntity;
    bool m_bState;
    bool m_bAlwaysUpdate;
    float32 m_flLightFOV;
    bool m_bEnableShadows;
    bool m_bSimpleProjection;
    bool m_bLightOnlyTarget;
    bool m_bLightWorld;
    bool m_bCameraSpace;
    float32 m_flBrightnessScale;
    Color m_LightColor;
    float32 m_flIntensity;
    float32 m_flLinearAttenuation;
    float32 m_flQuadraticAttenuation;
    bool m_bVolumetric;
    float32 m_flVolumetricIntensity;
    float32 m_flNoiseStrength;
    float32 m_flFlashlightTime;
    uint32 m_nNumPlanes;
    float32 m_flPlaneOffset;
    float32 m_flColorTransitionTime;
    float32 m_flAmbient;
    char[512] m_SpotlightTextureName;
    int32 m_nSpotlightTextureFrame;
    uint32 m_nShadowQuality;
    float32 m_flNearZ;
    float32 m_flFarZ;
    float32 m_flProjectionSize;
    float32 m_flRotation;
    bool m_bFlipHorizontal;
};

struct __declspec(align(8)) C_BaseFire {
    char m_pad[1384];
    float32 m_flScale;
    float32 m_flStartScale;
    float32 m_flScaleTime;
    uint32 m_nFlags;
};

struct TimedEvent {
    char m_pad[0];
    float32 m_TimeBetweenEvents;
    float32 m_fNextEvent;
};

struct CFireOverlay {
    char m_pad[208];
    C_FireSmoke* m_pOwner;
    Vector[4] m_vBaseColors;
    float32 m_flScale;
    int32 m_nGUID;
};

struct __declspec(align(8)) C_FireSmoke {
    char m_pad[1400];
    int32 m_nFlameModelIndex;
    int32 m_nFlameFromAboveModelIndex;
    float32 m_flScaleRegister;
    float32 m_flScaleStart;
    float32 m_flScaleEnd;
    GameTime_t m_flScaleTimeStart;
    GameTime_t m_flScaleTimeEnd;
    float32 m_flChildFlameSpread;
    float32 m_flClipPerc;
    bool m_bClipTested;
    bool m_bFadingOut;
    TimedEvent m_tParticleSpawn;
    CFireOverlay* m_pFireOverlay;
};

struct __declspec(align(8)) C_RopeKeyframe {
    char m_pad[3376];
    CBitVec< 10 > m_LinksTouchingSomething;
    int32 m_nLinksTouchingSomething;
    bool m_bApplyWind;
    int32 m_fPrevLockedPoints;
    int32 m_iForcePointMoveCounter;
    bool[2] m_bPrevEndPointPos;
    Vector[2] m_vPrevEndPointPos;
    float32 m_flCurScroll;
    float32 m_flScrollSpeed;
    uint16 m_RopeFlags;
    CStrongHandle< InfoForResourceTypeIMaterial2 > m_iRopeMaterialModelIndex;
    Vector[10] m_LightValues;
    uint8 m_nSegments;
    CHandle< C_BaseEntity > m_hStartPoint;
    CHandle< C_BaseEntity > m_hEndPoint;
    AttachmentHandle_t m_iStartAttachment;
    AttachmentHandle_t m_iEndAttachment;
    uint8 m_Subdiv;
    int16 m_RopeLength;
    int16 m_Slack;
    float32 m_TextureScale;
    uint8 m_fLockedPoints;
    uint8 m_nChangeCount;
    float32 m_Width;
    C_RopeKeyframe::CPhysicsDelegate m_PhysicsDelegate;
    CStrongHandle< InfoForResourceTypeIMaterial2 > m_hMaterial;
    int32 m_TextureHeight;
    Vector m_vecImpulse;
    Vector m_vecPreviousImpulse;
    float32 m_flCurrentGustTimer;
    float32 m_flCurrentGustLifetime;
    float32 m_flTimeToNextGust;
    Vector m_vWindDir;
    Vector m_vColorMod;
    Vector[2] m_vCachedEndPointAttachmentPos;
    QAngle[2] m_vCachedEndPointAttachmentAngle;
    bool m_bConstrainBetweenEndpoints;
    bitfield:1 m_bEndPointAttachmentPositionsDirty;
    bitfield:1 m_bEndPointAttachmentAnglesDirty;
    bitfield:1 m_bNewDataThisFrame;
    bitfield:1 m_bPhysicsInitted;
};

struct C_RopeKeyframe::CPhysicsDelegate {
    char m_pad[8];
    C_RopeKeyframe* m_pKeyframe;
};

struct C_SceneEntity::QueuedEvents_t {
    char m_pad[0];
    float32 starttime;
};

struct __declspec(align(8)) C_TintController {
};

struct CFlashlightEffect {
    char m_pad[16];
    bool m_bIsOn;
    bool m_bMuzzleFlashEnabled;
    float32 m_flMuzzleFlashBrightness;
    Quaternion m_quatMuzzleFlashOrientation;
    Vector m_vecMuzzleFlashOrigin;
    float32 m_flFov;
    float32 m_flFarZ;
    float32 m_flLinearAtten;
    bool m_bCastsShadows;
    float32 m_flCurrentPullBackDist;
    CStrongHandle< InfoForResourceTypeCTextureBase > m_FlashlightTexture;
    CStrongHandle< InfoForResourceTypeCTextureBase > m_MuzzleFlashTexture;
    char[64] m_textureName;
};

struct CInterpolatedValue {
    char m_pad[0];
    float32 m_flStartTime;
    float32 m_flEndTime;
    float32 m_flStartValue;
    float32 m_flEndValue;
    int32 m_nInterpType;
};

struct CGlowSprite {
    char m_pad[0];
    Vector m_vColor;
    float32 m_flHorzSize;
    float32 m_flVertSize;
    CStrongHandle< InfoForResourceTypeIMaterial2 > m_hMaterial;
};

struct CGlowOverlay {
    char m_pad[8];
    Vector m_vPos;
    bool m_bDirectional;
    Vector m_vDirection;
    bool m_bInSky;
    float32 m_skyObstructionScale;
    CGlowSprite[4] m_Sprites;
    int32 m_nSprites;
    float32 m_flProxyRadius;
    float32 m_flHDRColorScale;
    float32 m_flGlowObstructionScale;
    bool m_bCacheGlowObstruction;
    bool m_bCacheSkyObstruction;
    int16 m_bActivated;
    uint16 m_ListIndex;
    int32 m_queryHandle;
};

struct IClientAlphaProperty {
};

struct __declspec(align(8)) C_SkyCamera {
    char m_pad[1384];
    sky3dparams_t m_skyboxData;
    CUtlStringToken m_skyboxSlotToken;
    bool m_bUseAngles;
    C_SkyCamera* m_pNext;
};

struct __declspec(align(8)) CSkyboxReference {
    char m_pad[1384];
    WorldGroupId_t m_worldGroupId;
    CHandle< C_SkyCamera > m_hSkyCamera;
};

struct sky3dparams_t {
    char m_pad[8];
    int16 scale;
    Vector origin;
    bool bClip3DSkyBoxNearToWorldFar;
    float32 flClip3DSkyBoxNearToWorldFarOffset;
    fogparams_t fog;
    WorldGroupId_t m_nWorldGroupID;
};

struct VPhysicsCollisionAttribute_t {
    char m_pad[8];
    uint64 m_nInteractsAs;
    uint64 m_nInteractsWith;
    uint64 m_nInteractsExclude;
    uint32 m_nEntityId;
    uint32 m_nOwnerId;
    uint16 m_nHierarchyId;
    uint8 m_nCollisionGroup;
    uint8 m_nCollisionFunctionMask;
};

struct CDecalInfo {
    char m_pad[0];
    float32 m_flAnimationScale;
    float32 m_flAnimationLifeSpan;
    float32 m_flPlaceTime;
    float32 m_flFadeStartTime;
    float32 m_flFadeDuration;
    int32 m_nVBSlot;
    int32 m_nBoneIndex;
    Vector m_vPosition;
    float32 m_flBoundingRadiusSqr;
    CDecalInfo* m_pNext;
    CDecalInfo* m_pPrev;
    int32 m_nDecalMaterialIndex;
};

struct CEffectData {
    char m_pad[8];
    Vector m_vOrigin;
    Vector m_vStart;
    Vector m_vNormal;
    QAngle m_vAngles;
    CEntityHandle m_hEntity;
    CEntityHandle m_hOtherEntity;
    float32 m_flScale;
    float32 m_flMagnitude;
    float32 m_flRadius;
    CUtlStringToken m_nSurfaceProp;
    CWeakHandle< InfoForResourceTypeIParticleSystemDefinition > m_nEffectIndex;
    uint32 m_nDamageType;
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

struct __declspec(align(8)) C_EnvDetailController {
    char m_pad[1384];
    float32 m_flFadeStartDist;
    float32 m_flFadeEndDist;
};

struct C_EnvWindShared::WindAveEvent_t {
    char m_pad[0];
    float32 m_flStartWindSpeed;
    float32 m_flAveWindSpeed;
};

struct C_EnvWindShared::WindVariationEvent_t {
    char m_pad[0];
    float32 m_flWindAngleVariation;
    float32 m_flWindSpeedVariation;
};

struct __declspec(align(8)) C_InfoLadderDismount {
};

struct shard_model_desc_t {
    char m_pad[8];
    int32 m_nModelID;
    CStrongHandle< InfoForResourceTypeIMaterial2 > m_hMaterialBase;
    CStrongHandle< InfoForResourceTypeIMaterial2 > m_hMaterialDamageOverlay;
    ShardSolid_t m_solid;
    Vector2D m_vecPanelSize;
    Vector2D m_vecStressPositionA;
    Vector2D m_vecStressPositionB;
    C_NetworkUtlVectorBase< Vector2D > m_vecPanelVertices;
    C_NetworkUtlVectorBase< Vector4D > m_vInitialPanelVertices;
    float32 m_flGlassHalfThickness;
    bool m_bHasParent;
    bool m_bParentFrozen;
    CUtlStringToken m_SurfacePropStringToken;
};

struct __declspec(align(8)) C_GameRulesProxy {
};

struct C_GameRules {
    char m_pad[8];
    CNetworkVarChainer __m_pChainEntity;
    int32 m_nTotalPausedTicks;
    int32 m_nPauseStartTick;
    bool m_bGamePaused;
};

struct CGlowProperty {
    char m_pad[8];
    Vector m_fGlowColor;
    int32 m_iGlowType;
    int32 m_iGlowTeam;
    int32 m_nGlowRange;
    int32 m_nGlowRangeMin;
    Color m_glowColorOverride;
    bool m_bFlashing;
    float32 m_flGlowTime;
    float32 m_flGlowStartTime;
    bool m_bEligibleForScreenHighlight;
    bool m_bGlowing;
};

struct C_MultiplayRules {
};

struct __declspec(align(8)) PhysicsRagdollPose_t {
    char m_pad[8];
    C_NetworkUtlVectorBase< CTransform > m_Transforms;
    CHandle< C_BaseEntity > m_hOwner;
};

struct C_SingleplayRules {
};

struct __declspec(align(8)) C_SoundOpvarSetPointBase {
    char m_pad[1384];
    CUtlSymbolLarge m_iszStackName;
    CUtlSymbolLarge m_iszOperatorName;
    CUtlSymbolLarge m_iszOpvarName;
    int32 m_iOpvarIndex;
    bool m_bUseAutoCompare;
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

struct C_TeamplayRules {
};

struct __declspec(align(8)) C_TeamRoundTimer {
    char m_pad[1384];
    bool m_bTimerPaused;
    float32 m_flTimeRemaining;
    GameTime_t m_flTimerEndTime;
    bool m_bIsDisabled;
    bool m_bShowInHUD;
    int32 m_nTimerLength;
    int32 m_nTimerInitialLength;
    int32 m_nTimerMaxLength;
    bool m_bAutoCountdown;
    int32 m_nSetupTimeLength;
    int32 m_nState;
    bool m_bStartPaused;
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
    bool m_bFire1SecRemain;
    int32 m_nOldTimerLength;
    int32 m_nOldTimerState;
};

struct __declspec(align(8)) C_PortraitWorldCallbackHandler {
};

struct CEconItemAttribute {
    char m_pad[48];
    uint16 m_iAttributeDefinitionIndex;
    float32 m_flValue;
    float32 m_flInitialValue;
    int32 m_nRefundableCurrency;
    bool m_bSetBonus;
};

struct CAttributeManager {
    char m_pad[8];
    CUtlVector< CHandle< C_BaseEntity > > m_Providers;
    int32 m_iReapplyProvisionParity;
    CHandle< C_BaseEntity > m_hOuter;
    bool m_bPreventLoopback;
    attributeprovidertypes_t m_ProviderType;
    CUtlVector< CAttributeManager::cached_attribute_float_t > m_CachedResults;
};

struct CAttributeList {
    char m_pad[8];
    C_UtlVectorEmbeddedNetworkVar< CEconItemAttribute > m_Attributes;
    CAttributeManager* m_pManager;
};

struct CAttributeManager::cached_attribute_float_t {
    char m_pad[0];
    float32 flIn;
    CUtlSymbolLarge iAttribHook;
    float32 flOut;
};

struct C_EconItemView {
    char m_pad[96];
    bool m_bInventoryImageRgbaRequested;
    bool m_bInventoryImageTriedCache;
    int32 m_nInventoryImageRgbaWidth;
    int32 m_nInventoryImageRgbaHeight;
    char[260] m_szCurrentLoadCachedFileName;
    bool m_bRestoreCustomMaterialAfterPrecache;
    uint16 m_iItemDefinitionIndex;
    int32 m_iEntityQuality;
    uint32 m_iEntityLevel;
    uint64 m_iItemID;
    uint32 m_iItemIDHigh;
    uint32 m_iItemIDLow;
    uint32 m_iAccountID;
    uint32 m_iInventoryPosition;
    bool m_bInitialized;
    bool m_bDisallowSOC;
    bool m_bIsStoreItem;
    bool m_bIsTradeItem;
    int32 m_iEntityQuantity;
    int32 m_iRarityOverride;
    int32 m_iQualityOverride;
    int32 m_iOriginOverride;
    uint8 m_unClientFlags;
    uint8 m_unOverrideStyle;
    CAttributeList m_AttributeList;
    CAttributeList m_NetworkedDynamicAttributes;
    char[161] m_szCustomName;
    char[161] m_szCustomNameOverride;
    bool m_bInitializedTags;
};

struct C_AttributeContainer {
    char m_pad[80];
    C_EconItemView m_Item;
    int32 m_iExternalItemProviderRegisteredToken;
    uint64 m_ullRegisteredAsItemID;
};

struct C_EconEntity::AttachedModelData_t {
    char m_pad[0];
    int32 m_iModelDisplayFlags;
};

struct EntitySpottedState_t {
    char m_pad[8];
    bool m_bSpotted;
    uint32[2] m_bSpottedByMask;
};

struct C_CSGameRules {
    char m_pad[64];
    bool m_bFreezePeriod;
    bool m_bWarmupPeriod;
    GameTime_t m_fWarmupPeriodEnd;
    GameTime_t m_fWarmupPeriodStart;
    bool m_bServerPaused;
    bool m_bTerroristTimeOutActive;
    bool m_bCTTimeOutActive;
    float32 m_flTerroristTimeOutRemaining;
    float32 m_flCTTimeOutRemaining;
    int32 m_nTerroristTimeOuts;
    int32 m_nCTTimeOuts;
    bool m_bTechnicalTimeOut;
    bool m_bMatchWaitingForResume;
    int32 m_iRoundTime;
    float32 m_fMatchStartTime;
    GameTime_t m_fRoundStartTime;
    GameTime_t m_flRestartRoundTime;
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
    bool m_bIsQueuedMatchmaking;
    int32 m_nQueuedMatchmakingMode;
    bool m_bIsValveDS;
    bool m_bLogoMap;
    bool m_bPlayAllStepSoundsOnServer;
    int32 m_iSpectatorSlotCount;
    int32 m_MatchDevice;
    bool m_bHasMatchStarted;
    int32 m_nNextMapInMapgroup;
    char[512] m_szTournamentEventName;
    char[512] m_szTournamentEventStage;
    char[512] m_szMatchStatTxt;
    char[512] m_szTournamentPredictionsTxt;
    int32 m_nTournamentPredictionsPct;
    GameTime_t m_flCMMItemDropRevealStartTime;
    GameTime_t m_flCMMItemDropRevealEndTime;
    bool m_bIsDroppingItems;
    bool m_bIsQuestEligible;
    bool m_bIsHltvActive;
    uint16[100] m_arrProhibitedItemIndices;
    uint32[4] m_arrTournamentActiveCasterAccounts;
    int32 m_numBestOfMaps;
    int32 m_nHalloweenMaskListSeed;
    bool m_bBombDropped;
    bool m_bBombPlanted;
    int32 m_iRoundWinStatus;
    int32 m_eRoundWinReason;
    bool m_bTCantBuy;
    bool m_bCTCantBuy;
    int32[30] m_iMatchStats_RoundResults;
    int32[30] m_iMatchStats_PlayersAlive_CT;
    int32[30] m_iMatchStats_PlayersAlive_T;
    float32[32] m_TeamRespawnWaveTimes;
    GameTime_t[32] m_flNextRespawnWave;
    int32 m_nServerQuestID;
    Vector m_vMinimapMins;
    Vector m_vMinimapMaxs;
    float32[8] m_MinimapVerticalSectionHeights;
    bool m_bSpawnedTerrorHuntHeavy;
    int32[10] m_nEndMatchMapGroupVoteTypes;
    int32[10] m_nEndMatchMapGroupVoteOptions;
    int32 m_nEndMatchMapVoteWinner;
    int32 m_iNumConsecutiveCTLoses;
    int32 m_iNumConsecutiveTerroristLoses;
    bool m_bMarkClientStopRecordAtRoundEnd;
    int32 m_nMatchAbortedEarlyReason;
    bool m_bHasTriggeredRoundStartMusic;
    bool m_bSwitchingTeamsAtRoundReset;
    CCSGameModeRules* m_pGameModeRules;
    C_RetakeGameRules m_RetakeRules;
    uint8 m_nMatchEndCount;
    int32 m_nTTeamIntroVariant;
    int32 m_nCTTeamIntroVariant;
    bool m_bTeamIntroPeriod;
    int32 m_iRoundEndWinnerTeam;
    int32 m_eRoundEndReason;
    bool m_bRoundEndShowTimerDefend;
    int32 m_iRoundEndTimerTime;
    CUtlString m_sRoundEndFunFactToken;
    CPlayerSlot m_iRoundEndFunFactPlayerSlot;
    int32 m_iRoundEndFunFactData1;
    int32 m_iRoundEndFunFactData2;
    int32 m_iRoundEndFunFactData3;
    CUtlString m_sRoundEndMessage;
    int32 m_iRoundEndPlayerCount;
    bool m_bRoundEndNoMusic;
    int32 m_iRoundEndLegacy;
    uint8 m_nRoundEndCount;
    int32 m_iRoundStartRoundNumber;
    uint8 m_nRoundStartCount;
    float64 m_flLastPerfSampleTime;
};

struct __declspec(align(8)) C_CSGameRulesProxy {
    char m_pad[1384];
    C_CSGameRules* m_pGameRules;
};

struct __declspec(align(8)) CCSGameModeRules {
    char m_pad[8];
    CNetworkVarChainer __m_pChainEntity;
};

struct C_RetakeGameRules {
    char m_pad[248];
    int32 m_nMatchSeed;
    bool m_bBlockersPresent;
    bool m_bRoundInProgress;
    int32 m_iFirstSecondHalfRound;
    int32 m_iBombSite;
};

struct __declspec(align(8)) CCSGameModeRules_Noop {
};

struct __declspec(align(8)) CCSGameModeRules_ArmsRace {
    char m_pad[48];
    C_NetworkUtlVectorBase< CUtlString > m_WeaponSequence;
};

struct __declspec(align(8)) CCSGameModeRules_Deathmatch {
    char m_pad[48];
    GameTime_t m_flDMBonusStartTime;
    float32 m_flDMBonusTimeLength;
    CUtlString m_sDMBonusWeapon;
};

struct CSPerRoundStats_t {
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

struct CSMatchStats_t {
    char m_pad[104];
    int32 m_iEnemy5Ks;
    int32 m_iEnemy4Ks;
    int32 m_iEnemy3Ks;
    int32 m_iEnemyKnifeKills;
    int32 m_iEnemyTaserKills;
};

struct C_CSGO_TeamPreviewCharacterPosition {
    char m_pad[1384];
    int32 m_nVariant;
    int32 m_nRandom;
    int32 m_nOrdinal;
    CUtlString m_sWeaponName;
    uint64 m_xuid;
    C_EconItemView m_agentItem;
    C_EconItemView m_glovesItem;
    C_EconItemView m_weaponItem;
};

struct C_CSGO_TeamSelectCharacterPosition {
};

struct __declspec(align(8)) C_CSGO_TeamSelectTerroristPosition {
};

struct __declspec(align(8)) C_CSGO_TeamSelectCounterTerroristPosition {
};

struct C_CSGO_TeamIntroCharacterPosition {
};

struct __declspec(align(8)) C_CSGO_TeamIntroTerroristPosition {
};

struct __declspec(align(8)) C_CSGO_TeamIntroCounterTerroristPosition {
};

struct CCSGO_WingmanIntroCharacterPosition {
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

struct CCSPointScript {
    char m_pad[248];
    CCSPointScriptEntity* m_pParent;
};

struct CCSPointScriptExtensions_entity {
};

struct CCSPointScriptExtensions_player {
};

struct CCSPointScriptExtensions_observer {
};

struct CCSPointScriptExtensions_player_controller {
};

struct CCSPointScriptExtensions_weapon_cs_base {
};

struct CCSPointScriptExtensions_CCSWeaponBaseVData {
};

struct PredictedDamageTag_t {
    char m_pad[48];
    GameTick_t nTagTick;
    float32 flFlinchModSmall;
    float32 flFlinchModLarge;
    float32 flFriendlyFireDamageReductionRatio;
};

struct __declspec(align(16)) C_CSPlayerPawn {
    char m_pad[5400];
    CCSPlayer_BulletServices* m_pBulletServices;
    CCSPlayer_HostageServices* m_pHostageServices;
    CCSPlayer_BuyServices* m_pBuyServices;
    CCSPlayer_GlowServices* m_pGlowServices;
    CCSPlayer_ActionTrackingServices* m_pActionTrackingServices;
    CCSPlayer_DamageReactServices* m_pDamageReactServices;
    GameTime_t m_flHealthShotBoostExpirationTime;
    GameTime_t m_flLastFiredWeaponTime;
    bool m_bHasFemaleVoice;
    float32 m_flLandingTimeSeconds;
    float32 m_flOldFallVelocity;
    char[18] m_szLastPlaceName;
    bool m_bPrevDefuser;
    bool m_bPrevHelmet;
    int32 m_nPrevArmorVal;
    int32 m_nPrevGrenadeAmmoCount;
    uint32 m_unPreviousWeaponHash;
    uint32 m_unWeaponHash;
    bool m_bInBuyZone;
    bool m_bPreviouslyInBuyZone;
    QAngle m_aimPunchAngle;
    QAngle m_aimPunchAngleVel;
    int32 m_aimPunchTickBase;
    float32 m_aimPunchTickFraction;
    CUtlVector< QAngle > m_aimPunchCache;
    bool m_bInLanding;
    float32 m_flLandingStartTime;
    bool m_bInHostageRescueZone;
    bool m_bInBombZone;
    bool m_bIsBuyMenuOpen;
    GameTime_t m_flTimeOfLastInjury;
    GameTime_t m_flNextSprayDecalTime;
    int32 m_iRetakesOffering;
    int32 m_iRetakesOfferingCard;
    bool m_bRetakesHasDefuseKit;
    bool m_bRetakesMVPLastRound;
    int32 m_iRetakesMVPBoostItem;
    loadout_slot_t m_RetakesMVPBoostExtraUtility;
    bool m_bNeedToReApplyGloves;
    C_EconItemView m_EconGloves;
    uint8 m_nEconGlovesChanged;
    bool m_bMustSyncRagdollState;
    int32 m_nRagdollDamageBone;
    Vector m_vRagdollDamageForce;
    Vector m_vRagdollDamagePosition;
    char[64] m_szRagdollDamageWeaponName;
    bool m_bRagdollDamageHeadshot;
    Vector m_vRagdollServerOrigin;
    bool m_bLastHeadBoneTransformIsValid;
    GameTime_t m_lastLandTime;
    bool m_bOnGroundLastTick;
    QAngle m_qDeathEyeAngles;
    bool m_bSkipOneHeadConstraintUpdate;
    bool m_bLeftHanded;
    GameTime_t m_fSwitchedHandednessTime;
    float32 m_flViewmodelOffsetX;
    float32 m_flViewmodelOffsetY;
    float32 m_flViewmodelOffsetZ;
    float32 m_flViewmodelFOV;
    uint32[5] m_vecPlayerPatchEconIndices;
    Color m_GunGameImmunityColor;
    CUtlVector< C_BulletHitModel* > m_vecBulletHitModels;
    bool m_bIsWalking;
    QAngle m_thirdPersonHeading;
    float32 m_flSlopeDropOffset;
    float32 m_flSlopeDropHeight;
    Vector m_vHeadConstraintOffset;
    EntitySpottedState_t m_entitySpottedState;
    bool m_bIsScoped;
    bool m_bResumeZoom;
    bool m_bIsDefusing;
    bool m_bIsGrabbingHostage;
    CSPlayerBlockingUseAction_t m_iBlockingUseActionInProgress;
    GameTime_t m_flEmitSoundTime;
    bool m_bInNoDefuseArea;
    int32 m_nWhichBombZone;
    int32 m_iShotsFired;
    float32 m_flFlinchStack;
    float32 m_flVelocityModifier;
    float32 m_flHitHeading;
    int32 m_nHitBodyPart;
    bool m_bWaitForNoAttack;
    float32 m_ignoreLadderJumpTime;
    bool m_bKilledByHeadshot;
    int32 m_ArmorValue;
    uint16 m_unCurrentEquipmentValue;
    uint16 m_unRoundStartEquipmentValue;
    uint16 m_unFreezetimeEndEquipmentValue;
    CEntityIndex m_nLastKillerIndex;
    bool m_bOldIsScoped;
    bool m_bHasDeathInfo;
    float32 m_flDeathInfoTime;
    Vector m_vecDeathInfoOrigin;
    GameTime_t m_grenadeParameterStashTime;
    bool m_bGrenadeParametersStashed;
    QAngle m_angStashedShootAngles;
    Vector m_vecStashedGrenadeThrowPosition;
    Vector m_vecStashedVelocity;
    QAngle[2] m_angShootAngleHistory;
    Vector[2] m_vecThrowPositionHistory;
    Vector[2] m_vecVelocityHistory;
    C_UtlVectorEmbeddedNetworkVar< PredictedDamageTag_t > m_PredictedDamageTags;
    GameTick_t m_nPrevHighestReceivedDamageTagTick;
    int32 m_nHighestAppliedDamageTagTick;
};

struct __declspec(align(8)) C_PlayerPing {
    char m_pad[1432];
    CHandle< C_CSPlayerPawn > m_hPlayer;
    CHandle< C_BaseEntity > m_hPingedEntity;
    int32 m_iType;
    bool m_bUrgent;
    char[18] m_szPlaceName;
};

struct CCSPlayer_PingServices {
    char m_pad[64];
    CHandle< C_BaseEntity > m_hPlayerPing;
};

struct __declspec(align(8)) C_CSPlayerResource {
    char m_pad[1384];
    bool[12] m_bHostageAlive;
    bool[12] m_isHostageFollowingSomeone;
    CEntityIndex[12] m_iHostageEntityIDs;
    Vector m_bombsiteCenterA;
    Vector m_bombsiteCenterB;
    int32[4] m_hostageRescueX;
    int32[4] m_hostageRescueY;
    int32[4] m_hostageRescueZ;
    bool m_bEndMatchNextMapAllVoted;
    bool m_foundGoalPositions;
};

struct CCSPlayer_DamageReactServices {
};

struct CPlayer_ViewModelServices {
};

struct CCSPlayerBase_CameraServices {
    char m_pad[528];
    uint32 m_iFOV;
    uint32 m_iFOVStart;
    GameTime_t m_flFOVTime;
    float32 m_flFOVRate;
    CHandle< C_BaseEntity > m_hZoomOwner;
    float32 m_flLastShotFOV;
};

struct WeaponPurchaseCount_t {
    char m_pad[48];
    uint16 m_nItemDefIndex;
    uint16 m_nCount;
};

struct WeaponPurchaseTracker_t {
    char m_pad[8];
    C_UtlVectorEmbeddedNetworkVar< WeaponPurchaseCount_t > m_weaponPurchases;
};

struct CCSPlayer_ActionTrackingServices {
    char m_pad[64];
    CHandle< C_BasePlayerWeapon > m_hLastWeaponBeforeC4AutoSwitch;
    bool m_bIsRescuing;
    WeaponPurchaseTracker_t m_weaponPurchasesThisMatch;
    WeaponPurchaseTracker_t m_weaponPurchasesThisRound;
};

struct CCSPlayer_BulletServices {
    char m_pad[64];
    int32 m_totalHitsOnServer;
};

struct SellbackPurchaseEntry_t {
    char m_pad[48];
    uint16 m_unDefIdx;
    int32 m_nCost;
    int32 m_nPrevArmor;
    bool m_bPrevHelmet;
    CEntityHandle m_hItem;
};

struct CCSPlayer_BuyServices {
    char m_pad[64];
    C_UtlVectorEmbeddedNetworkVar< SellbackPurchaseEntry_t > m_vecSellbackPurchaseEntries;
};

struct CCSPlayer_CameraServices {
    char m_pad[552];
    float32 m_flDeathCamTilt;
    Vector m_vClientScopeInaccuracy;
};

struct CCSPlayer_HostageServices {
    char m_pad[64];
    CHandle< C_BaseEntity > m_hCarriedHostage;
    CHandle< C_BaseEntity > m_hCarriedHostageProp;
};

struct CCSPlayer_ItemServices {
    char m_pad[64];
    bool m_bHasDefuser;
    bool m_bHasHelmet;
    bool m_bHasHeavyArmor;
};

struct CCSPlayer_MovementServices {
    char m_pad[536];
    float32 m_flMaxFallVelocity;
    Vector m_vecLadderNormal;
    int32 m_nLadderSurfacePropIndex;
    float32 m_flDuckAmount;
    float32 m_flDuckSpeed;
    bool m_bDuckOverride;
    bool m_bDesiresDuck;
    float32 m_flDuckOffset;
    uint32 m_nDuckTimeMsecs;
    uint32 m_nDuckJumpTimeMsecs;
    uint32 m_nJumpTimeMsecs;
    float32 m_flLastDuckTime;
    Vector2D m_vecLastPositionAtFullCrouchSpeed;
    bool m_duckUntilOnGround;
    bool m_bHasWalkMovedSinceLastJump;
    bool m_bInStuckTest;
    float32[64][2] m_flStuckCheckTime;
    int32 m_nTraceCount;
    int32 m_StuckLast;
    bool m_bSpeedCropped;
    float32 m_flGroundMoveEfficiency;
    int32 m_nOldWaterLevel;
    float32 m_flWaterEntryTime;
    Vector m_vecForward;
    Vector m_vecLeft;
    Vector m_vecUp;
    int32 m_nGameCodeHasMovedPlayerAfterCommand;
    bool m_bOldJumpPressed;
    float32 m_flJumpPressedTime;
    float32 m_flJumpUntil;
    float32 m_flJumpVel;
    GameTime_t m_fStashGrenadeParameterWhen;
    uint64 m_nButtonDownMaskPrev;
    float32 m_flOffsetTickCompleteTime;
    float32 m_flOffsetTickStashedSpeed;
    float32 m_flStamina;
    float32 m_flHeightAtJumpStart;
    float32 m_flMaxJumpHeightThisJump;
    float32 m_flMaxJumpHeightLastJump;
};

struct CCSPlayer_UseServices {
};

struct __declspec(align(8)) C_BaseViewModel {
    char m_pad[3984];
    Vector m_vecLastFacing;
    uint32 m_nViewModelIndex;
    uint32 m_nAnimationParity;
    float32 m_flAnimationStartTime;
    CHandle< C_BasePlayerWeapon > m_hWeapon;
    CUtlSymbolLarge m_sVMName;
    CUtlSymbolLarge m_sAnimationPrefix;
    AttachmentHandle_t m_iCameraAttachment;
    QAngle m_vecLastCameraAngles;
    float32 m_previousElapsedDuration;
    float32 m_previousCycle;
    int32 m_nOldAnimationParity;
    HSequence m_hOldLayerSequence;
    int32 m_oldLayer;
    float32 m_oldLayerStartTime;
    CHandle< C_BaseEntity > m_hControlPanel;
};

struct CCSPlayer_ViewModelServices {
    char m_pad[64];
    CHandle< C_BaseViewModel >[3] m_hViewModel;
};

struct CCSPlayer_WaterServices {
    char m_pad[64];
    float32 m_flWaterJumpTime;
    Vector m_vecWaterJumpVel;
    float32 m_flSwimSoundTime;
};

struct CCSPlayer_WeaponServices {
    char m_pad[184];
    GameTime_t m_flNextAttack;
    bool m_bIsLookingAtWeapon;
    bool m_bIsHoldingLookAtWeapon;
    uint32 m_nOldShootPositionHistoryCount;
    uint32 m_nOldInputHistoryCount;
};

struct CCSObserver_ObserverServices {
    char m_pad[88];
    CEntityHandle m_hLastObserverTarget;
    Vector m_vecObserverInterpolateOffset;
    Vector m_vecObserverInterpStartPos;
    float32 m_flObsInterp_PathLength;
    Quaternion m_qObsInterp_OrientationStart;
    Quaternion m_qObsInterp_OrientationTravelDir;
    ObserverInterpState_t m_obsInterpState;
    bool m_bObserverInterpolationNeedsDeferredSetup;
};

struct CCSObserver_CameraServices {
};

struct CCSObserver_MovementServices {
};

struct CCSObserver_UseServices {
};

struct CCSObserver_ViewModelServices {
};

struct CCSPlayerController_ActionTrackingServices {
    char m_pad[64];
    C_UtlVectorEmbeddedNetworkVar< CSPerRoundStats_t > m_perRoundStats;
    CSMatchStats_t m_matchStats;
    int32 m_iNumRoundKills;
    int32 m_iNumRoundKillsHeadshots;
    uint32 m_unTotalRoundDamageDealt;
};

struct __declspec(align(8)) CCSPlayerController {
    char m_pad[1824];
    CCSPlayerController_InGameMoneyServices* m_pInGameMoneyServices;
    CCSPlayerController_InventoryServices* m_pInventoryServices;
    CCSPlayerController_ActionTrackingServices* m_pActionTrackingServices;
    CCSPlayerController_DamageServices* m_pDamageServices;
    uint32 m_iPing;
    bool m_bHasCommunicationAbuseMute;
    CUtlSymbolLarge m_szCrosshairCodes;
    uint8 m_iPendingTeamNum;
    GameTime_t m_flForceTeamTime;
    int32 m_iCompTeammateColor;
    bool m_bEverPlayedOnTeam;
    GameTime_t m_flPreviousForceJoinTeamTime;
    CUtlSymbolLarge m_szClan;
    CUtlString m_sSanitizedPlayerName;
    int32 m_iCoachingTeam;
    uint64 m_nPlayerDominated;
    uint64 m_nPlayerDominatingMe;
    int32 m_iCompetitiveRanking;
    int32 m_iCompetitiveWins;
    int8 m_iCompetitiveRankType;
    int32 m_iCompetitiveRankingPredicted_Win;
    int32 m_iCompetitiveRankingPredicted_Loss;
    int32 m_iCompetitiveRankingPredicted_Tie;
    int32 m_nEndMatchNextMapVote;
    uint16 m_unActiveQuestId;
    QuestProgress::Reason m_nQuestProgressReason;
    uint32 m_unPlayerTvControlFlags;
    int32 m_iDraftIndex;
    uint32 m_msQueuedModeDisconnectionTimestamp;
    uint32 m_uiAbandonRecordedReason;
    bool m_bCannotBeKicked;
    bool m_bEverFullyConnected;
    bool m_bAbandonAllowsSurrender;
    bool m_bAbandonOffersInstantSurrender;
    bool m_bDisconnection1MinWarningPrinted;
    bool m_bScoreReported;
    int32 m_nDisconnectionTick;
    bool m_bControllingBot;
    bool m_bHasControlledBotThisRound;
    bool m_bHasBeenControlledByPlayerThisRound;
    int32 m_nBotsControlledThisRound;
    bool m_bCanControlObservedBot;
    CHandle< C_CSPlayerPawn > m_hPlayerPawn;
    CHandle< C_CSObserverPawn > m_hObserverPawn;
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
    C_NetworkUtlVectorBase< EKillTypes_t > m_vecKills;
    bool m_bMvpNoMusic;
    int32 m_eMvpReason;
    int32 m_iMusicKitID;
    int32 m_iMusicKitMVPs;
    int32 m_iMVPs;
    bool m_bIsPlayerNameDirty;
};

struct CDamageRecord {
    char m_pad[40];
    CHandle< C_CSPlayerPawn > m_PlayerDamager;
    CHandle< C_CSPlayerPawn > m_PlayerRecipient;
    CHandle< CCSPlayerController > m_hPlayerControllerDamager;
    CHandle< CCSPlayerController > m_hPlayerControllerRecipient;
    CUtlString m_szPlayerDamagerName;
    CUtlString m_szPlayerRecipientName;
    uint64 m_DamagerXuid;
    uint64 m_RecipientXuid;
    int32 m_iBulletsDamage;
    int32 m_iDamage;
    int32 m_iActualHealthRemoved;
    int32 m_iNumHits;
    int32 m_iLastBulletUpdate;
    bool m_bIsOtherEnemy;
    EKillTypes_t m_killType;
};

struct CCSPlayerController_DamageServices {
    char m_pad[64];
    int32 m_nSendUpdate;
    C_UtlVectorEmbeddedNetworkVar< CDamageRecord > m_DamageList;
};

struct CCSPlayerController_InGameMoneyServices {
    char m_pad[64];
    int32 m_iAccount;
    int32 m_iStartAccount;
    int32 m_iTotalCashSpent;
    int32 m_iCashSpentThisRound;
};

struct ServerAuthoritativeWeaponSlot_t {
    char m_pad[40];
    uint16 unClass;
    uint16 unSlot;
    uint16 unItemDefIdx;
};

struct CCSPlayerController_InventoryServices {
    char m_pad[64];
    uint16 m_unMusicID;
    MedalRank_t[6] m_rank;
    int32 m_nPersonaDataPublicLevel;
    int32 m_nPersonaDataPublicCommendsLeader;
    int32 m_nPersonaDataPublicCommendsTeacher;
    int32 m_nPersonaDataPublicCommendsFriendly;
    int32 m_nPersonaDataXpTrailLevel;
    C_UtlVectorEmbeddedNetworkVar< ServerAuthoritativeWeaponSlot_t > m_vecServerAuthoritativeWeaponSlots;
};

struct C_IronSightController {
    char m_pad[16];
    bool m_bIronSightAvailable;
    float32 m_flIronSightAmount;
    float32 m_flIronSightAmountGained;
    float32 m_flIronSightAmountBiased;
    float32 m_flIronSightAmount_Interpolated;
    float32 m_flIronSightAmountGained_Interpolated;
    float32 m_flIronSightAmountBiased_Interpolated;
    float32 m_flInterpolationLastUpdated;
    QAngle[8] m_angDeltaAverage;
    QAngle m_angViewLast;
    Vector2D m_vecDotCoords;
    float32 m_flDotBlur;
    float32 m_flSpeedRatio;
};

struct __declspec(align(8)) CompositeMaterialMatchFilter_t {
    char m_pad[0];
    CompositeMaterialMatchFilterType_t m_nCompositeMaterialMatchFilterType;
    CUtlString m_strMatchFilter;
    CUtlString m_strMatchValue;
    bool m_bPassWhenTrue;
};

struct __declspec(align(8)) CompositeMaterialInputLooseVariable_t {
    char m_pad[0];
    CUtlString m_strName;
    bool m_bExposeExternally;
    CUtlString m_strExposedFriendlyName;
    CUtlString m_strExposedFriendlyGroupName;
    bool m_bExposedVariableIsFixedRange;
    CUtlString m_strExposedVisibleWhenTrue;
    CUtlString m_strExposedHiddenWhenTrue;
    CompositeMaterialInputLooseVariableType_t m_nVariableType;
    bool m_bValueBoolean;
    int32 m_nValueIntX;
    int32 m_nValueIntY;
    int32 m_nValueIntZ;
    int32 m_nValueIntW;
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
    CompositeMaterialVarSystemVar_t m_nValueSystemVar;
    CResourceName m_strResourceMaterial;
    CUtlString m_strTextureContentAssetPath;
    CResourceName m_strTextureRuntimeResourcePath;
    CUtlString m_strTextureCompilationVtexTemplate;
    CompositeMaterialInputTextureType_t m_nTextureType;
    CUtlString m_strString;
    CUtlString m_strPanoramaPanelPath;
    int32 m_nPanoramaRenderRes;
};

struct __declspec(align(8)) CompMatMutatorCondition_t {
    char m_pad[0];
    CompMatPropertyMutatorConditionType_t m_nMutatorCondition;
    CUtlString m_strMutatorConditionContainerName;
    CUtlString m_strMutatorConditionContainerVarName;
    CUtlString m_strMutatorConditionContainerVarValue;
    bool m_bPassWhenTrue;
};

struct __declspec(align(8)) CompMatPropertyMutator_t {
    char m_pad[0];
    bool m_bEnabled;
    CompMatPropertyMutatorType_t m_nMutatorCommandType;
    CUtlString m_strInitWith_Container;
    CUtlString m_strCopyProperty_InputContainerSrc;
    CUtlString m_strCopyProperty_InputContainerProperty;
    CUtlString m_strCopyProperty_TargetProperty;
    CUtlString m_strRandomRollInputVars_SeedInputVar;
    CUtlVector< CUtlString > m_vecRandomRollInputVars_InputVarsToRoll;
    CUtlString m_strCopyMatchingKeys_InputContainerSrc;
    CUtlString m_strCopyKeysWithSuffix_InputContainerSrc;
    CUtlString m_strCopyKeysWithSuffix_FindSuffix;
    CUtlString m_strCopyKeysWithSuffix_ReplaceSuffix;
    CompositeMaterialInputLooseVariable_t m_nSetValue_Value;
    CUtlString m_strGenerateTexture_TargetParam;
    CUtlString m_strGenerateTexture_InitialContainer;
    int32 m_nResolution;
    bool m_bIsScratchTarget;
    bool m_bSplatDebugInfo;
    bool m_bCaptureInRenderDoc;
    CUtlVector< CompMatPropertyMutator_t > m_vecTexGenInstructions;
    CUtlVector< CompMatPropertyMutator_t > m_vecConditionalMutators;
    CUtlString m_strPopInputQueue_Container;
    CUtlString m_strDrawText_InputContainerSrc;
    CUtlString m_strDrawText_InputContainerProperty;
    Vector2D m_vecDrawText_Position;
    Color m_colDrawText_Color;
    CUtlString m_strDrawText_Font;
    CUtlVector< CompMatMutatorCondition_t > m_vecConditions;
};

struct __declspec(align(8)) CompositeMaterialInputContainer_t {
    char m_pad[0];
    bool m_bEnabled;
    CompositeMaterialInputContainerSourceType_t m_nCompositeMaterialInputContainerSourceType;
    CResourceName m_strSpecificContainerMaterial;
    CUtlString m_strAttrName;
    CUtlString m_strAlias;
    CUtlVector< CompositeMaterialInputLooseVariable_t > m_vecLooseVariables;
    CUtlString m_strAttrNameForVar;
    bool m_bExposeExternally;
};

struct __declspec(align(8)) CompositeMaterialAssemblyProcedure_t {
    char m_pad[0];
    CUtlVector< CResourceName > m_vecCompMatIncludes;
    CUtlVector< CompositeMaterialMatchFilter_t > m_vecMatchFilters;
    CUtlVector< CompositeMaterialInputContainer_t > m_vecCompositeInputContainers;
    CUtlVector< CompMatPropertyMutator_t > m_vecPropertyMutators;
};

struct GeneratedTextureHandle_t {
    char m_pad[0];
    CUtlString m_strBitmapName;
};

struct CompositeMaterial_t {
    char m_pad[8];
    KeyValues3 m_TargetKVs;
    KeyValues3 m_PreGenerationKVs;
    KeyValues3 m_FinalKVs;
    CUtlVector< GeneratedTextureHandle_t > m_vecGeneratedTextures;
};

struct __declspec(align(8)) CompositeMaterialEditorPoint_t {
    char m_pad[0];
    CResourceName m_ModelName;
    int32 m_nSequenceIndex;
    float32 m_flCycle;
    KeyValues3 m_KVModelStateChoices;
    bool m_bEnableChildModel;
    CResourceName m_ChildModelName;
    CUtlVector< CompositeMaterialAssemblyProcedure_t > m_vecCompositeMaterialAssemblyProcedures;
    CUtlVector< CompositeMaterial_t > m_vecCompositeMaterials;
};

struct __declspec(align(8)) CCompositeMaterialEditorDoc {
    char m_pad[8];
    int32 m_nVersion;
    CUtlVector< CompositeMaterialEditorPoint_t > m_Points;
    KeyValues3 m_KVthumbnail;
};

struct CGlobalLightBase {
    char m_pad[16];
    bool m_bSpotLight;
    Vector m_SpotLightOrigin;
    QAngle m_SpotLightAngles;
    Vector m_ShadowDirection;
    Vector m_AmbientDirection;
    Vector m_SpecularDirection;
    Vector m_InspectorSpecularDirection;
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
    bool m_bBackgroundClearNotRequired;
    float32 m_flCloudScale;
    float32 m_flCloud1Speed;
    float32 m_flCloud1Direction;
    float32 m_flCloud2Speed;
    float32 m_flCloud2Direction;
    float32 m_flAmbientScale1;
    float32 m_flAmbientScale2;
    float32 m_flGroundScale;
    float32 m_flLightScale;
    float32 m_flFoWDarkness;
    bool m_bEnableSeparateSkyboxFog;
    Vector m_vFowColor;
    Vector m_ViewOrigin;
    QAngle m_ViewAngles;
    float32 m_flViewFoV;
    Vector[8] m_WorldPoints;
    Vector2D m_vFogOffsetLayer0;
    Vector2D m_vFogOffsetLayer1;
    CHandle< C_BaseEntity > m_hEnvWind;
    CHandle< C_BaseEntity > m_hEnvSky;
};

struct __declspec(align(16)) C_GlobalLight {
    char m_pad[2608];
    uint16 m_WindClothForceHandle;
};

struct C_CSGO_PreviewModel_GraphController {
    char m_pad[96];
    CAnimGraphParamOptionalRef< char* > m_pszCharacterMode;
    CAnimGraphParamOptionalRef< char* > m_pszWeaponState;
    CAnimGraphParamOptionalRef< char* > m_pszWeaponType;
    CAnimGraphParamOptionalRef< char* > m_pszEndOfMatchCelebration;
};

struct C_CSGO_PreviewPlayer_GraphController {
    char m_pad[96];
    CAnimGraphParamOptionalRef< char* > m_pszCharacterMode;
    CAnimGraphParamOptionalRef< char* > m_pszTeamPreviewVariant;
    CAnimGraphParamOptionalRef< char* > m_pszTeamPreviewPosition;
    CAnimGraphParamOptionalRef< char* > m_pszEndOfMatchCelebration;
    CAnimGraphParamOptionalRef< int32 > m_nTeamPreviewRandom;
    CAnimGraphParamOptionalRef< char* > m_pszWeaponState;
    CAnimGraphParamOptionalRef< char* > m_pszWeaponType;
    CAnimGraphParamOptionalRef< bool > m_bCT;
};

struct __declspec(align(8)) C_CSGO_MapPreviewCameraPathNode {
    char m_pad[1384];
    CUtlSymbolLarge m_szParentPathUniqueID;
    int32 m_nPathIndex;
    Vector m_vInTangentLocal;
    Vector m_vOutTangentLocal;
    float32 m_flFOV;
    float32 m_flCameraSpeed;
    float32 m_flEaseIn;
    float32 m_flEaseOut;
    Vector m_vInTangentWorld;
    Vector m_vOutTangentWorld;
};

struct __declspec(align(8)) C_CSGO_MapPreviewCameraPath {
    char m_pad[1384];
    float32 m_flZFar;
    float32 m_flZNear;
    bool m_bLoop;
    bool m_bVerticalFOV;
    bool m_bConstantSpeed;
    float32 m_flDuration;
    float32 m_flPathLength;
    float32 m_flPathDuration;
};

struct CCSPlayer_GlowServices {
};

struct __declspec(align(8)) C_VoteController {
    char m_pad[1400];
    int32 m_iActiveIssueIndex;
    int32 m_iOnlyTeamToVote;
    int32[5] m_nVoteOptionCount;
    int32 m_nPotentialVotes;
    bool m_bVotesDirty;
    bool m_bTypeDirty;
    bool m_bIsYesNoVote;
};

struct __declspec(align(8)) C_MapVetoPickController {
    char m_pad[1400];
    int32 m_nDraftType;
    int32 m_nTeamWinningCoinToss;
    int32[64] m_nTeamWithFirstChoice;
    int32[7] m_nVoteMapIdsList;
    int32[64] m_nAccountIDs;
    int32[64] m_nMapId0;
    int32[64] m_nMapId1;
    int32[64] m_nMapId2;
    int32[64] m_nMapId3;
    int32[64] m_nMapId4;
    int32[64] m_nMapId5;
    int32[64] m_nStartingSide0;
    int32 m_nCurrentPhase;
    int32 m_nPhaseStartTick;
    int32 m_nPhaseDurationTicks;
    int32 m_nPostDataUpdateTick;
    bool m_bDisabledHud;
};

struct CPlayerSprayDecalRenderHelper {
};

struct C_CSGO_TeamPreviewCamera {
    char m_pad[1488];
    int32 m_nVariant;
    bool m_bDofEnabled;
    float32 m_flDofNearBlurry;
    float32 m_flDofNearCrisp;
    float32 m_flDofFarCrisp;
    float32 m_flDofFarBlurry;
    float32 m_flDofTiltToGround;
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

struct C_CSGO_EndOfMatchLineupEndpoint {
};

struct __declspec(align(8)) C_CSGO_EndOfMatchLineupStart {
};

struct __declspec(align(8)) C_CSGO_EndOfMatchLineupEnd {
};

struct __declspec(align(8)) C_CsmFovOverride {
    char m_pad[1384];
    CUtlString m_cameraName;
    float32 m_flCsmFovOverrideValue;
};

struct C_Chicken_GraphController {
    char m_pad[96];
    CAnimGraphParamRef< char* > m_paramActivity;
    CAnimGraphParamRef< bool > m_paramEndActivityImmediately;
    CAnimGraphParamRef< bool > m_paramSnapToSquatting;
    CAnimGraphTagRef m_sActivityFinished;
    float32 m_flSquatProbability;
};

struct __declspec(align(8)) C_PointEntity {
};

struct __declspec(align(8)) C_EnvCombinedLightProbeVolume {
    char m_pad[5576];
    Color m_Entity_Color;
    float32 m_Entity_flBrightness;
    CStrongHandle< InfoForResourceTypeCTextureBase > m_Entity_hCubemapTexture;
    bool m_Entity_bCustomCubemapTexture;
    CStrongHandle< InfoForResourceTypeCTextureBase > m_Entity_hLightProbeTexture;
    CStrongHandle< InfoForResourceTypeCTextureBase > m_Entity_hLightProbeDirectLightIndicesTexture;
    CStrongHandle< InfoForResourceTypeCTextureBase > m_Entity_hLightProbeDirectLightScalarsTexture;
    CStrongHandle< InfoForResourceTypeCTextureBase > m_Entity_hLightProbeDirectLightShadowsTexture;
    Vector m_Entity_vBoxMins;
    Vector m_Entity_vBoxMaxs;
    bool m_Entity_bMoveable;
    int32 m_Entity_nHandshake;
    int32 m_Entity_nEnvCubeMapArrayIndex;
    int32 m_Entity_nPriority;
    bool m_Entity_bStartDisabled;
    float32 m_Entity_flEdgeFadeDist;
    Vector m_Entity_vEdgeFadeDists;
    int32 m_Entity_nLightProbeSizeX;
    int32 m_Entity_nLightProbeSizeY;
    int32 m_Entity_nLightProbeSizeZ;
    int32 m_Entity_nLightProbeAtlasX;
    int32 m_Entity_nLightProbeAtlasY;
    int32 m_Entity_nLightProbeAtlasZ;
    bool m_Entity_bEnabled;
};

struct __declspec(align(8)) C_EnvCubemap {
    char m_pad[1512];
    CStrongHandle< InfoForResourceTypeCTextureBase > m_Entity_hCubemapTexture;
    bool m_Entity_bCustomCubemapTexture;
    float32 m_Entity_flInfluenceRadius;
    Vector m_Entity_vBoxProjectMins;
    Vector m_Entity_vBoxProjectMaxs;
    bool m_Entity_bMoveable;
    int32 m_Entity_nHandshake;
    int32 m_Entity_nEnvCubeMapArrayIndex;
    int32 m_Entity_nPriority;
    float32 m_Entity_flEdgeFadeDist;
    Vector m_Entity_vEdgeFadeDists;
    float32 m_Entity_flDiffuseScale;
    bool m_Entity_bStartDisabled;
    bool m_Entity_bDefaultEnvMap;
    bool m_Entity_bDefaultSpecEnvMap;
    bool m_Entity_bIndoorCubeMap;
    bool m_Entity_bCopyDiffuseFromDefaultCubemap;
    bool m_Entity_bEnabled;
};

struct __declspec(align(8)) C_EnvCubemapBox {
};

struct __declspec(align(8)) C_EnvCubemapFog {
    char m_pad[1384];
    float32 m_flEndDistance;
    float32 m_flStartDistance;
    float32 m_flFogFalloffExponent;
    bool m_bHeightFogEnabled;
    float32 m_flFogHeightWidth;
    float32 m_flFogHeightEnd;
    float32 m_flFogHeightStart;
    float32 m_flFogHeightExponent;
    float32 m_flLODBias;
    bool m_bActive;
    bool m_bStartDisabled;
    float32 m_flFogMaxOpacity;
    int32 m_nCubemapSourceType;
    CStrongHandle< InfoForResourceTypeIMaterial2 > m_hSkyMaterial;
    CUtlSymbolLarge m_iszSkyEntity;
    CStrongHandle< InfoForResourceTypeCTextureBase > m_hFogCubemapTexture;
    bool m_bHasHeightFogEnd;
    bool m_bFirstTime;
};

struct __declspec(align(8)) C_GradientFog {
    char m_pad[1384];
    CStrongHandle< InfoForResourceTypeCTextureBase > m_hGradientFogTexture;
    float32 m_flFogStartDistance;
    float32 m_flFogEndDistance;
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

struct __declspec(align(8)) C_EnvLightProbeVolume {
    char m_pad[5448];
    CStrongHandle< InfoForResourceTypeCTextureBase > m_Entity_hLightProbeTexture;
    CStrongHandle< InfoForResourceTypeCTextureBase > m_Entity_hLightProbeDirectLightIndicesTexture;
    CStrongHandle< InfoForResourceTypeCTextureBase > m_Entity_hLightProbeDirectLightScalarsTexture;
    CStrongHandle< InfoForResourceTypeCTextureBase > m_Entity_hLightProbeDirectLightShadowsTexture;
    Vector m_Entity_vBoxMins;
    Vector m_Entity_vBoxMaxs;
    bool m_Entity_bMoveable;
    int32 m_Entity_nHandshake;
    int32 m_Entity_nPriority;
    bool m_Entity_bStartDisabled;
    int32 m_Entity_nLightProbeSizeX;
    int32 m_Entity_nLightProbeSizeY;
    int32 m_Entity_nLightProbeSizeZ;
    int32 m_Entity_nLightProbeAtlasX;
    int32 m_Entity_nLightProbeAtlasY;
    int32 m_Entity_nLightProbeAtlasZ;
    bool m_Entity_bEnabled;
};

struct __declspec(align(8)) C_PlayerVisibility {
    char m_pad[1384];
    float32 m_flVisibilityStrength;
    float32 m_flFogDistanceMultiplier;
    float32 m_flFogMaxDensityMultiplier;
    float32 m_flFadeTime;
    bool m_bStartDisabled;
    bool m_bIsEnabled;
};

struct __declspec(align(8)) C_EnvVolumetricFogController {
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
    Vector m_vBoxMins;
    Vector m_vBoxMaxs;
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
    bool m_bIsMaster;
    CStrongHandle< InfoForResourceTypeCTextureBase > m_hFogIndirectTexture;
    int32 m_nForceRefreshCount;
    float32 m_fNoiseSpeed;
    float32 m_fNoiseStrength;
    Vector m_vNoiseScale;
    bool m_bFirstTime;
};

struct __declspec(align(8)) C_EnvVolumetricFogVolume {
    char m_pad[1384];
    bool m_bActive;
    Vector m_vBoxMins;
    Vector m_vBoxMaxs;
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

struct __declspec(align(8)) CInfoTarget {
};

struct __declspec(align(8)) CInfoParticleTarget {
};

struct __declspec(align(8)) C_InfoVisibilityBox {
    char m_pad[1388];
    int32 m_nMode;
    Vector m_vBoxSize;
    bool m_bEnabled;
};

struct __declspec(align(8)) CInfoWorldLayer {
    char m_pad[1384];
    CEntityIOOutput m_pOutputOnEntitiesSpawned;
    CUtlSymbolLarge m_worldName;
    CUtlSymbolLarge m_layerName;
    bool m_bWorldLayerVisible;
    bool m_bEntitiesSpawned;
    bool m_bCreateAsChildSpawnGroup;
    uint32 m_hLayerSpawnGroup;
    bool m_bWorldLayerActuallyVisible;
};

struct __declspec(align(8)) CPointChildModifier {
    char m_pad[1384];
    bool m_bOrphanInsteadOfDeletingChildrenOnRemove;
};

struct __declspec(align(8)) C_PointCameraVFOV {
    char m_pad[1480];
    float32 m_flVerticalFOV;
};

struct __declspec(align(8)) CPointTemplate {
    char m_pad[1384];
    CUtlSymbolLarge m_iszWorldName;
    CUtlSymbolLarge m_iszSource2EntityLumpName;
    CUtlSymbolLarge m_iszEntityFilterName;
    float32 m_flTimeoutInterval;
    bool m_bAsynchronouslySpawnEntities;
    CEntityIOOutput m_pOutputOnSpawned;
    PointTemplateClientOnlyEntityBehavior_t m_clientOnlyEntityBehavior;
    PointTemplateOwnerSpawnGroupType_t m_ownerSpawnGroupType;
    CUtlVector< uint32 > m_createdSpawnGroupHandles;
    CUtlVector< CEntityHandle > m_SpawnedEntityHandles;
    HSCRIPT m_ScriptSpawnCallback;
    HSCRIPT m_ScriptCallbackScope;
};

struct __declspec(align(8)) CRagdollManager {
    char m_pad[1384];
    int8 m_iCurrentMaxRagdollCount;
};

struct C_SoundAreaEntityBase {
    char m_pad[1384];
    bool m_bDisabled;
    bool m_bWasEnabled;
    CUtlSymbolLarge m_iszSoundAreaType;
    Vector m_vPos;
};

struct __declspec(align(8)) C_SoundAreaEntitySphere {
    char m_pad[1424];
    float32 m_flRadius;
};

struct __declspec(align(8)) C_SoundAreaEntityOrientedBox {
    char m_pad[1424];
    Vector m_vMin;
    Vector m_vMax;
};

struct __declspec(align(8)) C_SoundEventEntity {
    char m_pad[1384];
    bool m_bStartOnSpawn;
    bool m_bToLocalPlayer;
    bool m_bStopOnNew;
    bool m_bSaveRestore;
    bool m_bSavedIsPlaying;
    float32 m_flSavedElapsedTime;
    CUtlSymbolLarge m_iszSourceEntityName;
    CUtlSymbolLarge m_iszAttachmentName;
    CEntityOutputTemplate< uint64 > m_onGUIDChanged;
    CEntityIOOutput m_onSoundFinished;
    float32 m_flClientCullRadius;
    CUtlSymbolLarge m_iszSoundName;
    CEntityHandle m_hSource;
    int32 m_nEntityIndexSelection;
    bitfield:1 m_bClientSideOnly;
};

struct __declspec(align(8)) C_SoundEventEntityAlias_snd_event_point {
};

struct __declspec(align(8)) C_SoundEventAABBEntity {
    char m_pad[1576];
    Vector m_vMins;
    Vector m_vMaxs;
};

struct __declspec(align(8)) C_SoundEventOBBEntity {
    char m_pad[1576];
    Vector m_vMins;
    Vector m_vMaxs;
};

struct __declspec(align(8)) C_SoundEventSphereEntity {
    char m_pad[1576];
    float32 m_flRadius;
};

struct __declspec(align(8)) C_SoundEventPathCornerEntity {
    char m_pad[1576];
    C_NetworkUtlVectorBase< SoundeventPathCornerPairNetworked_t > m_vecCornerPairsNetworked;
};

struct __declspec(align(8)) C_BasePlayerPawn {
    char m_pad[4520];
    CPlayer_WeaponServices* m_pWeaponServices;
    CPlayer_ItemServices* m_pItemServices;
    CPlayer_AutoaimServices* m_pAutoaimServices;
    CPlayer_ObserverServices* m_pObserverServices;
    CPlayer_WaterServices* m_pWaterServices;
    CPlayer_UseServices* m_pUseServices;
    CPlayer_FlashlightServices* m_pFlashlightServices;
    CPlayer_CameraServices* m_pCameraServices;
    CPlayer_MovementServices* m_pMovementServices;
    C_UtlVectorEmbeddedNetworkVar< ViewAngleServerChange_t > m_ServerViewAngleChanges;
    uint32 m_nHighestConsumedServerViewAngleChangeIndex;
    QAngle v_angle;
    QAngle v_anglePrevious;
    uint32 m_iHideHUD;
    sky3dparams_t m_skybox3d;
    GameTime_t m_flDeathTime;
    Vector m_vecPredictionError;
    GameTime_t m_flPredictionErrorTime;
    Vector m_vecLastCameraSetupLocalOrigin;
    GameTime_t m_flLastCameraSetupTime;
    float32 m_flFOVSensitivityAdjust;
    float32 m_flMouseSensitivity;
    Vector m_vOldOrigin;
    float32 m_flOldSimulationTime;
    int32 m_nLastExecutedCommandNumber;
    int32 m_nLastExecutedCommandTick;
    CHandle< CBasePlayerController > m_hController;
    bool m_bIsSwappingToPredictableController;
};

struct __declspec(align(8)) C_Team {
    char m_pad[1384];
    C_NetworkUtlVectorBase< CHandle< CBasePlayerController > > m_aPlayerControllers;
    C_NetworkUtlVectorBase< CHandle< C_BasePlayerPawn > > m_aPlayers;
    int32 m_iScore;
    char[129] m_szTeamname;
};

struct __declspec(align(8)) CBasePlayerVData {
    char m_pad[40];
    CResourceNameTyped< CWeakHandle< InfoForResourceTypeCModel > > m_sModelName;
    CSkillFloat m_flHeadDamageMultiplier;
    CSkillFloat m_flChestDamageMultiplier;
    CSkillFloat m_flStomachDamageMultiplier;
    CSkillFloat m_flArmDamageMultiplier;
    CSkillFloat m_flLegDamageMultiplier;
    float32 m_flHoldBreathTime;
    float32 m_flDrowningDamageInterval;
    int32 m_nDrowningDamageInitial;
    int32 m_nDrowningDamageMax;
    int32 m_nWaterSpeed;
    float32 m_flUseRange;
    float32 m_flUseAngleTolerance;
    float32 m_flCrouchTime;
};

struct __declspec(align(8)) CBasePlayerWeaponVData {
    char m_pad[40];
    CResourceNameTyped< CWeakHandle< InfoForResourceTypeCModel > > m_szWorldModel;
    CResourceNameTyped< CWeakHandle< InfoForResourceTypeCModel > > m_sToolsOnlyOwnerModelName;
    bool m_bBuiltRightHanded;
    bool m_bAllowFlipping;
    CAttachmentNameSymbolWithStorage m_sMuzzleAttachment;
    CResourceNameTyped< CWeakHandle< InfoForResourceTypeIParticleSystemDefinition > > m_szMuzzleFlashParticle;
    bool m_bLinkedCooldowns;
    ItemFlagTypes_t m_iFlags;
    AmmoIndex_t m_nPrimaryAmmoType;
    AmmoIndex_t m_nSecondaryAmmoType;
    int32 m_iMaxClip1;
    int32 m_iMaxClip2;
    int32 m_iDefaultClip1;
    int32 m_iDefaultClip2;
    bool m_bReserveAmmoAsClips;
    int32 m_iWeight;
    bool m_bAutoSwitchTo;
    bool m_bAutoSwitchFrom;
    RumbleEffect_t m_iRumbleEffect;
    int32 m_iSlot;
    int32 m_iPosition;
    CUtlOrderedMap< WeaponSound_t, CSoundEventName > m_aShootSounds;
};

struct CClientAlphaProperty {
    char m_pad[16];
    uint8 m_nRenderFX;
    uint8 m_nRenderMode;
    bitfield:1 m_bAlphaOverride;
    bitfield:1 m_bShadowAlphaOverride;
    bitfield:6 m_nReserved;
    uint8 m_nAlpha;
    uint16 m_nDesyncOffset;
    uint16 m_nReserved2;
    uint16 m_nDistFadeStart;
    uint16 m_nDistFadeEnd;
    float32 m_flFadeScale;
    GameTime_t m_flRenderFxStartTime;
    float32 m_flRenderFxDuration;
};

struct __declspec(align(8)) CServerOnlyModelEntity {
};

struct __declspec(align(8)) C_ModelPointEntity {
};

struct __declspec(align(8)) CLogicRelay {
    char m_pad[1384];
    CEntityIOOutput m_OnTrigger;
    CEntityIOOutput m_OnSpawn;
    bool m_bDisabled;
    bool m_bWaitForRefire;
    bool m_bTriggerOnce;
    bool m_bFastRetrigger;
    bool m_bPassthoughCaller;
};

struct __declspec(align(8)) C_ParticleSystem {
    char m_pad[3368];
    char[512] m_szSnapshotFileName;
    bool m_bActive;
    bool m_bFrozen;
    float32 m_flFreezeTransitionDuration;
    int32 m_nStopType;
    bool m_bAnimateDuringGameplayPause;
    CStrongHandle< InfoForResourceTypeIParticleSystemDefinition > m_iEffectIndex;
    GameTime_t m_flStartTime;
    float32 m_flPreSimTime;
    Vector[4] m_vServerControlPoints;
    uint8[4] m_iServerControlPointAssignments;
    CHandle< C_BaseEntity >[64] m_hControlPointEnts;
    bool m_bNoSave;
    bool m_bNoFreeze;
    bool m_bNoRamp;
    bool m_bStartActive;
    CUtlSymbolLarge m_iszEffectName;
    CUtlSymbolLarge[64] m_iszControlPointNames;
    int32 m_nDataCP;
    Vector m_vecDataCPValue;
    int32 m_nTintCP;
    Color m_clrTint;
    bool m_bOldActive;
    bool m_bOldFrozen;
};

struct __declspec(align(8)) C_PathParticleRope {
    char m_pad[1392];
    bool m_bStartActive;
    float32 m_flMaxSimulationTime;
    CUtlSymbolLarge m_iszEffectName;
    CUtlVector< CUtlSymbolLarge > m_PathNodes_Name;
    float32 m_flParticleSpacing;
    float32 m_flSlack;
    float32 m_flRadius;
    Color m_ColorTint;
    int32 m_nEffectState;
    CStrongHandle< InfoForResourceTypeIParticleSystemDefinition > m_iEffectIndex;
    C_NetworkUtlVectorBase< Vector > m_PathNodes_Position;
    C_NetworkUtlVectorBase< Vector > m_PathNodes_TangentIn;
    C_NetworkUtlVectorBase< Vector > m_PathNodes_TangentOut;
    C_NetworkUtlVectorBase< Vector > m_PathNodes_Color;
    C_NetworkUtlVectorBase< bool > m_PathNodes_PinEnabled;
    C_NetworkUtlVectorBase< float32 > m_PathNodes_RadiusScale;
};

struct __declspec(align(8)) C_PathParticleRopeAlias_path_particle_rope_clientside {
};

struct __declspec(align(8)) CPathSimple {
    char m_pad[1472];
    CUtlString m_pathString;
};

struct __declspec(align(8)) C_DynamicLight {
    char m_pad[3368];
    uint8 m_Flags;
    uint8 m_LightStyle;
    float32 m_Radius;
    int32 m_Exponent;
    float32 m_InnerAngle;
    float32 m_OuterAngle;
    float32 m_SpotRadius;
};

struct __declspec(align(8)) C_EnvScreenOverlay {
    char m_pad[1384];
    CUtlSymbolLarge[10] m_iszOverlayNames;
    float32[10] m_flOverlayTimes;
    GameTime_t m_flStartTime;
    int32 m_iDesiredOverlay;
    bool m_bIsActive;
    bool m_bWasActive;
    int32 m_iCachedDesiredOverlay;
    int32 m_iCurrentOverlay;
    GameTime_t m_flCurrentOverlayTime;
};

struct __declspec(align(8)) C_FuncTrackTrain {
    char m_pad[3368];
    int32 m_nLongAxis;
    float32 m_flRadius;
    float32 m_flLineLength;
};

struct C_LightGlowOverlay {
    char m_pad[208];
    Vector m_vecOrigin;
    Vector m_vecDirection;
    int32 m_nMinDist;
    int32 m_nMaxDist;
    int32 m_nOuterMaxDist;
    bool m_bOneSided;
    bool m_bModulateByDot;
};

struct __declspec(align(8)) C_LightGlow {
    char m_pad[3368];
    uint32 m_nHorizontalSize;
    uint32 m_nVerticalSize;
    uint32 m_nMinDist;
    uint32 m_nMaxDist;
    uint32 m_nOuterMaxDist;
    float32 m_flGlowProxySize;
    float32 m_flHDRColorScale;
    C_LightGlowOverlay m_GlowOverlay;
};

struct __declspec(align(8)) C_SpotlightEnd {
    char m_pad[3368];
    float32 m_flLightScale;
    float32 m_Radius;
};

struct __declspec(align(8)) C_PointValueRemapper {
    char m_pad[1384];
    bool m_bDisabled;
    bool m_bDisabledOld;
    bool m_bUpdateOnClient;
    ValueRemapperInputType_t m_nInputType;
    CHandle< C_BaseEntity > m_hRemapLineStart;
    CHandle< C_BaseEntity > m_hRemapLineEnd;
    float32 m_flMaximumChangePerSecond;
    float32 m_flDisengageDistance;
    float32 m_flEngageDistance;
    bool m_bRequiresUseKey;
    ValueRemapperOutputType_t m_nOutputType;
    C_NetworkUtlVectorBase< CHandle< C_BaseEntity > > m_hOutputEntities;
    ValueRemapperHapticsType_t m_nHapticsType;
    ValueRemapperMomentumType_t m_nMomentumType;
    float32 m_flMomentumModifier;
    float32 m_flSnapValue;
    float32 m_flCurrentMomentum;
    ValueRemapperRatchetType_t m_nRatchetType;
    float32 m_flRatchetOffset;
    float32 m_flInputOffset;
    bool m_bEngaged;
    bool m_bFirstUpdate;
    float32 m_flPreviousValue;
    GameTime_t m_flPreviousUpdateTickTime;
    Vector m_vecPreviousTestPoint;
};

struct __declspec(align(8)) C_PointWorldText {
    char m_pad[3376];
    bool m_bForceRecreateNextUpdate;
    char[512] m_messageText;
    char[64] m_FontName;
    bool m_bEnabled;
    bool m_bFullbright;
    float32 m_flWorldUnitsPerPx;
    float32 m_flFontSize;
    float32 m_flDepthOffset;
    Color m_Color;
    PointWorldTextJustifyHorizontal_t m_nJustifyHorizontal;
    PointWorldTextJustifyVertical_t m_nJustifyVertical;
    PointWorldTextReorientMode_t m_nReorientMode;
};

struct __declspec(align(8)) CCitadelSoundOpvarSetOBB {
    char m_pad[1408];
    CUtlSymbolLarge m_iszStackName;
    CUtlSymbolLarge m_iszOperatorName;
    CUtlSymbolLarge m_iszOpvarName;
    Vector m_vDistanceInnerMins;
    Vector m_vDistanceInnerMaxs;
    Vector m_vDistanceOuterMins;
    Vector m_vDistanceOuterMaxs;
    int32 m_nAABBDirection;
};

struct __declspec(align(8)) C_HandleTest {
    char m_pad[1384];
    CHandle< C_BaseEntity > m_Handle;
    bool m_bSendHandle;
};

struct __declspec(align(8)) C_EnvWind {
    char m_pad[1384];
    C_EnvWindShared m_EnvWindShared;
};

struct __declspec(align(8)) C_BaseToggle {
};

struct __declspec(align(8)) C_BaseButton {
    char m_pad[3368];
    CHandle< C_BaseModelEntity > m_glowEntity;
    bool m_usable;
    CUtlSymbolLarge m_szDisplayText;
};

struct __declspec(align(8)) C_PrecipitationBlocker {
};

struct __declspec(align(8)) C_EntityDissolve {
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
    Vector m_vDissolverOrigin;
    uint32 m_nMagnitude;
    bool m_bCoreExplode;
    bool m_bLinkedToServerEnt;
};

struct __declspec(align(8)) C_EnvProjectedTexture {
};

struct __declspec(align(8)) C_EnvDecal {
    char m_pad[3368];
    CStrongHandle< InfoForResourceTypeIMaterial2 > m_hDecalMaterial;
    float32 m_flWidth;
    float32 m_flHeight;
    float32 m_flDepth;
    uint32 m_nRenderOrder;
    bool m_bProjectOnWorld;
    bool m_bProjectOnCharacters;
    bool m_bProjectOnWater;
    float32 m_flDepthSortBias;
};

struct __declspec(align(8)) C_FuncBrush {
};

struct __declspec(align(8)) C_FuncElectrifiedVolume {
    char m_pad[3368];
    ParticleIndex_t m_nAmbientEffect;
    CUtlSymbolLarge m_EffectName;
    bool m_bState;
};

struct __declspec(align(8)) C_FuncRotating {
};

struct __declspec(align(8)) C_Breakable {
};

struct __declspec(align(8)) C_PhysBox {
};

struct __declspec(align(8)) C_BaseFlex {
    char m_pad[3992];
    C_NetworkUtlVectorBase< float32 > m_flexWeight;
    Vector m_vLookTargetPosition;
    bool m_blinktoggle;
    int32 m_nLastFlexUpdateFrameCount;
    Vector m_CachedViewTarget;
    SceneEventId_t m_nNextSceneEventId;
    int32 m_iBlink;
    float32 m_blinktime;
    bool m_prevblinktoggle;
    int32 m_iJawOpen;
    float32 m_flJawOpenAmount;
    float32 m_flBlinkAmount;
    AttachmentHandle_t m_iMouthAttachment;
    AttachmentHandle_t m_iEyeAttachment;
    bool m_bResetFlexWeightsOnModelChange;
    int32 m_nEyeOcclusionRendererBone;
    matrix3x4_t m_mEyeOcclusionRendererCameraToBoneTransform;
    Vector m_vEyeOcclusionRendererHalfExtent;
    C_BaseFlex::Emphasized_Phoneme[3] m_PhonemeClasses;
};

struct __declspec(align(8)) C_SceneEntity {
    char m_pad[1392];
    bool m_bIsPlayingBack;
    bool m_bPaused;
    bool m_bMultiplayer;
    bool m_bAutogenerated;
    float32 m_flForceClientTime;
    uint16 m_nSceneStringIndex;
    bool m_bClientOnly;
    CHandle< C_BaseFlex > m_hOwner;
    C_NetworkUtlVectorBase< CHandle< C_BaseFlex > > m_hActorList;
    bool m_bWasPlaying;
    CUtlVector< C_SceneEntity::QueuedEvents_t > m_QueuedEvents;
    float32 m_flCurrentTime;
};

struct C_SunGlowOverlay {
    char m_pad[208];
    bool m_bModulateByDot;
};

struct __declspec(align(8)) C_Sun {
    char m_pad[3368];
    ParticleIndex_t m_fxSSSunFlareEffectIndex;
    ParticleIndex_t m_fxSunFlareEffectIndex;
    float32 m_fdistNormalize;
    Vector m_vSunPos;
    Vector m_vDirection;
    CUtlSymbolLarge m_iszEffectName;
    CUtlSymbolLarge m_iszSSEffectName;
    Color m_clrOverlay;
    bool m_bOn;
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

struct __declspec(align(8)) C_BaseTrigger {
    char m_pad[3368];
    bool m_bDisabled;
    bool m_bClientSidePredicted;
};

struct __declspec(align(8)) C_TriggerVolume {
};

struct __declspec(align(8)) C_TriggerMultiple {
};

struct __declspec(align(8)) C_TriggerLerpObject {
};

struct __declspec(align(8)) C_TriggerPhysics {
    char m_pad[3376];
    float32 m_gravityScale;
    float32 m_linearLimit;
    float32 m_linearDamping;
    float32 m_angularLimit;
    float32 m_angularDamping;
    float32 m_linearForce;
    float32 m_flFrequency;
    float32 m_flDampingRatio;
    Vector m_vecLinearForcePointAt;
    bool m_bCollapseToForcePoint;
    Vector m_vecLinearForcePointAtWorld;
    Vector m_vecLinearForceDirection;
    bool m_bConvertToDebrisWhenPossible;
};

struct __declspec(align(8)) C_Beam {
    char m_pad[3368];
    float32 m_flFrameRate;
    float32 m_flHDRColorScale;
    GameTime_t m_flFireTime;
    float32 m_flDamage;
    uint8 m_nNumBeamEnts;
    int32 m_queryHandleHalo;
    CStrongHandle< InfoForResourceTypeIMaterial2 > m_hBaseMaterial;
    CStrongHandle< InfoForResourceTypeIMaterial2 > m_nHaloIndex;
    BeamType_t m_nBeamType;
    uint32 m_nBeamFlags;
    CHandle< C_BaseEntity >[10] m_hAttachEntity;
    AttachmentHandle_t[10] m_nAttachIndex;
    float32 m_fWidth;
    float32 m_fEndWidth;
    float32 m_fFadeLength;
    float32 m_fHaloScale;
    float32 m_fAmplitude;
    float32 m_fStartFrame;
    float32 m_fSpeed;
    float32 m_flFrame;
    BeamClipStyle_t m_nClipStyle;
    bool m_bTurnedOff;
    Vector m_vecEndPos;
    CHandle< C_BaseEntity > m_hEndEntity;
};

struct __declspec(align(8)) C_FuncLadder {
    char m_pad[3368];
    Vector m_vecLadderDir;
    CUtlVector< CHandle< C_InfoLadderDismount > > m_Dismounts;
    Vector m_vecLocalTop;
    Vector m_vecPlayerMountPositionTop;
    Vector m_vecPlayerMountPositionBottom;
    float32 m_flAutoRideSpeed;
    bool m_bDisabled;
    bool m_bFakeLadder;
    bool m_bHasSlack;
};

struct __declspec(align(8)) CPrecipitationVData {
    char m_pad[40];
    CResourceNameTyped< CWeakHandle< InfoForResourceTypeIParticleSystemDefinition > > m_szParticlePrecipitationEffect;
    float32 m_flInnerDistance;
    ParticleAttachment_t m_nAttachType;
    bool m_bBatchSameVolumeType;
    int32 m_nRTEnvCP;
    int32 m_nRTEnvCPComponent;
    CUtlString m_szModifier;
};

struct __declspec(align(8)) C_Sprite {
    char m_pad[3368];
    CStrongHandle< InfoForResourceTypeIMaterial2 > m_hSpriteMaterial;
    CHandle< C_BaseEntity > m_hAttachedToEntity;
    AttachmentHandle_t m_nAttachment;
    float32 m_flSpriteFramerate;
    float32 m_flFrame;
    GameTime_t m_flDieTime;
    uint32 m_nBrightness;
    float32 m_flBrightnessDuration;
    float32 m_flSpriteScale;
    float32 m_flScaleDuration;
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
    GameTime_t m_flBrightnessTimeStart;
    CWeakHandle< InfoForResourceTypeIMaterial2 > m_hOldSpriteMaterial;
    int32 m_nSpriteWidth;
    int32 m_nSpriteHeight;
};

struct __declspec(align(8)) CSpriteOriented {
};

struct C_BaseClientUIEntity {
    char m_pad[3376];
    bool m_bEnabled;
    CUtlSymbolLarge m_DialogXMLName;
    CUtlSymbolLarge m_PanelClassName;
    CUtlSymbolLarge m_PanelID;
};

struct __declspec(align(8)) C_PointClientUIDialog {
    char m_pad[3416];
    CHandle< C_BaseEntity > m_hActivator;
    bool m_bStartEnabled;
};

struct __declspec(align(8)) C_PointClientUIHUD {
    char m_pad[3424];
    bool m_bCheckCSSClasses;
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
    bool m_bAllowInteractionFromAllSceneWorlds;
    C_NetworkUtlVectorBase< CUtlSymbolLarge > m_vecCSSClasses;
};

struct __declspec(align(16)) CPointOffScreenIndicatorUi {
    char m_pad[3984];
    bool m_bBeenEnabled;
    bool m_bHide;
    float32 m_flSeenTargetTime;
    C_PointClientUIWorldPanel* m_pTargetPanel;
};

struct __declspec(align(16)) C_PointClientUIWorldPanel {
    char m_pad[3424];
    bool m_bForceRecreateNextUpdate;
    bool m_bMoveViewToPlayerNextThink;
    bool m_bCheckCSSClasses;
    CTransform m_anchorDeltaTransform;
    CPointOffScreenIndicatorUi* m_pOffScreenIndicator;
    bool m_bIgnoreInput;
    bool m_bLit;
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
    bool m_bAllowInteractionFromAllSceneWorlds;
    C_NetworkUtlVectorBase< CUtlSymbolLarge > m_vecCSSClasses;
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

struct __declspec(align(16)) C_PointClientUIWorldTextPanel {
    char m_pad[3984];
    char[512] m_messageText;
};

struct __declspec(align(8)) CInfoOffscreenPanoramaTexture {
    char m_pad[1384];
    bool m_bDisabled;
    int32 m_nResolutionX;
    int32 m_nResolutionY;
    CUtlSymbolLarge m_szLayoutFileName;
    CUtlSymbolLarge m_RenderAttrName;
    C_NetworkUtlVectorBase< CHandle< C_BaseModelEntity > > m_TargetEntities;
    int32 m_nTargetChangeCount;
    C_NetworkUtlVectorBase< CUtlSymbolLarge > m_vecCSSClasses;
    bool m_bCheckCSSClasses;
};

struct __declspec(align(8)) CBombTarget {
    char m_pad[3376];
    bool m_bBombPlantedHere;
};

struct __declspec(align(8)) CHostageRescueZoneShim {
};

struct __declspec(align(8)) CHostageRescueZone {
};

struct __declspec(align(8)) C_TriggerBuoyancy {
    char m_pad[3376];
    CBuoyancyHelper m_BuoyancyHelper;
    float32 m_flFluidDensity;
};

struct __declspec(align(8)) CFuncWater {
    char m_pad[3368];
    CBuoyancyHelper m_BuoyancyHelper;
};

struct __declspec(align(8)) CWaterSplasher {
};

struct __declspec(align(8)) C_InfoInstructorHintHostageRescueZone {
};

struct __declspec(align(8)) C_CSObserverPawn {
    char m_pad[5392];
    CEntityHandle m_hDetectParentChange;
};

struct __declspec(align(8)) C_FootstepControl {
    char m_pad[3376];
    CUtlSymbolLarge m_source;
    CUtlSymbolLarge m_destination;
};

struct __declspec(align(8)) CCSWeaponBaseVData {
    char m_pad[840];
    CSWeaponType m_WeaponType;
    CSWeaponCategory m_WeaponCategory;
    CResourceNameTyped< CWeakHandle< InfoForResourceTypeCModel > > m_szViewModel;
    CResourceNameTyped< CWeakHandle< InfoForResourceTypeCModel > > m_szPlayerModel;
    CResourceNameTyped< CWeakHandle< InfoForResourceTypeCModel > > m_szWorldDroppedModel;
    CResourceNameTyped< CWeakHandle< InfoForResourceTypeCModel > > m_szAimsightLensMaskModel;
    CResourceNameTyped< CWeakHandle< InfoForResourceTypeCModel > > m_szMagazineModel;
    CResourceNameTyped< CWeakHandle< InfoForResourceTypeIParticleSystemDefinition > > m_szHeatEffect;
    CResourceNameTyped< CWeakHandle< InfoForResourceTypeIParticleSystemDefinition > > m_szEjectBrassEffect;
    CResourceNameTyped< CWeakHandle< InfoForResourceTypeIParticleSystemDefinition > > m_szMuzzleFlashParticleAlt;
    CResourceNameTyped< CWeakHandle< InfoForResourceTypeIParticleSystemDefinition > > m_szMuzzleFlashThirdPersonParticle;
    CResourceNameTyped< CWeakHandle< InfoForResourceTypeIParticleSystemDefinition > > m_szMuzzleFlashThirdPersonParticleAlt;
    CResourceNameTyped< CWeakHandle< InfoForResourceTypeIParticleSystemDefinition > > m_szTracerParticle;
    gear_slot_t m_GearSlot;
    int32 m_GearSlotPosition;
    loadout_slot_t m_DefaultLoadoutSlot;
    CUtlString m_sWrongTeamMsg;
    int32 m_nPrice;
    int32 m_nKillAward;
    int32 m_nPrimaryReserveAmmoMax;
    int32 m_nSecondaryReserveAmmoMax;
    bool m_bMeleeWeapon;
    bool m_bHasBurstMode;
    bool m_bIsRevolver;
    bool m_bCannotShootUnderwater;
    CGlobalSymbol m_szName;
    CUtlString m_szAnimExtension;
    CSWeaponSilencerType m_eSilencerType;
    int32 m_nCrosshairMinDistance;
    int32 m_nCrosshairDeltaDistance;
    bool m_bIsFullAuto;
    int32 m_nNumBullets;
    CFiringModeFloat m_flCycleTime;
    CFiringModeFloat m_flMaxSpeed;
    CFiringModeFloat m_flSpread;
    CFiringModeFloat m_flInaccuracyCrouch;
    CFiringModeFloat m_flInaccuracyStand;
    CFiringModeFloat m_flInaccuracyJump;
    CFiringModeFloat m_flInaccuracyLand;
    CFiringModeFloat m_flInaccuracyLadder;
    CFiringModeFloat m_flInaccuracyFire;
    CFiringModeFloat m_flInaccuracyMove;
    CFiringModeFloat m_flRecoilAngle;
    CFiringModeFloat m_flRecoilAngleVariance;
    CFiringModeFloat m_flRecoilMagnitude;
    CFiringModeFloat m_flRecoilMagnitudeVariance;
    CFiringModeInt m_nTracerFrequency;
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
    float32 m_flBotAudibleRange;
    CUtlString m_szUseRadioSubtitle;
    bool m_bUnzoomsAfterShot;
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
    QAngle m_angPivotAngle;
    Vector m_vecIronSightEyePos;
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
    Vector m_vSmokeColor;
    CGlobalSymbol m_szAnimClass;
};

struct __declspec(align(8)) C_PlayerSprayDecal {
    char m_pad[3368];
    int32 m_nUniqueID;
    uint32 m_unAccountID;
    uint32 m_unTraceID;
    uint32 m_rtGcTime;
    Vector m_vecEndPos;
    Vector m_vecStart;
    Vector m_vecLeft;
    Vector m_vecNormal;
    int32 m_nPlayer;
    int32 m_nEntity;
    int32 m_nHitbox;
    float32 m_flCreationTime;
    int32 m_nTintID;
    uint8 m_nVersion;
    uint8[128] m_ubSignature;
    CPlayerSprayDecalRenderHelper m_SprayRenderHelper;
};

struct __declspec(align(8)) C_FuncConveyor {
    char m_pad[3376];
    Vector m_vecMoveDirEntitySpace;
    float32 m_flTargetSpeed;
    GameTick_t m_nTransitionStartTick;
    int32 m_nTransitionDurationTicks;
    float32 m_flTransitionStartSpeed;
    C_NetworkUtlVectorBase< CHandle< C_BaseEntity > > m_hConveyorModels;
    float32 m_flCurrentConveyorOffset;
    float32 m_flCurrentConveyorSpeed;
};

struct __declspec(align(16)) CGrenadeTracer {
    char m_pad[3392];
    float32 m_flTracerDuration;
    GrenadeType_t m_nType;
};

struct __declspec(align(16)) C_Inferno {
    char m_pad[3432];
    ParticleIndex_t m_nfxFireDamageEffect;
    CStrongHandle< InfoForResourceTypeIParticleSnapshot > m_hInfernoPointsSnapshot;
    CStrongHandle< InfoForResourceTypeIParticleSnapshot > m_hInfernoFillerPointsSnapshot;
    CStrongHandle< InfoForResourceTypeIParticleSnapshot > m_hInfernoOutlinePointsSnapshot;
    CStrongHandle< InfoForResourceTypeIParticleSnapshot > m_hInfernoClimbingOutlinePointsSnapshot;
    CStrongHandle< InfoForResourceTypeIParticleSnapshot > m_hInfernoDecalsSnapshot;
    Vector[64] m_firePositions;
    Vector[64] m_fireParentPositions;
    bool[64] m_bFireIsBurning;
    Vector[64] m_BurnNormal;
    int32 m_fireCount;
    int32 m_nInfernoType;
    float32 m_nFireLifetime;
    bool m_bInPostEffectTime;
    int32 m_lastFireCount;
    int32 m_nFireEffectTickBegin;
    int32 m_drawableCount;
    bool m_blosCheck;
    int32 m_nlosperiod;
    float32 m_maxFireHalfWidth;
    float32 m_maxFireHeight;
    Vector m_minBounds;
    Vector m_maxBounds;
    float32 m_flLastGrassBurnThink;
};

struct __declspec(align(16)) C_FireCrackerBlast {
};

struct __declspec(align(8)) C_BarnLight {
    char m_pad[3368];
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
    float32 m_flLuminaireAnisotropy;
    CUtlString m_LightStyleString;
    GameTime_t m_flLightStyleStartTime;
    C_NetworkUtlVectorBase< CUtlString > m_QueuedLightStyleStrings;
    C_NetworkUtlVectorBase< CUtlString > m_LightStyleEvents;
    C_NetworkUtlVectorBase< CHandle< C_BaseModelEntity > > m_LightStyleTargets;
    CEntityIOOutput[4] m_StyleEvent;
    CStrongHandle< InfoForResourceTypeCTextureBase > m_hLightCookie;
    float32 m_flShape;
    float32 m_flSoftX;
    float32 m_flSoftY;
    float32 m_flSkirt;
    float32 m_flSkirtNear;
    Vector m_vSizeParams;
    float32 m_flRange;
    Vector m_vShear;
    int32 m_nBakeSpecularToCubemaps;
    Vector m_vBakeSpecularToCubemapsSize;
    int32 m_nCastShadows;
    int32 m_nShadowMapSize;
    int32 m_nShadowPriority;
    bool m_bContactShadow;
    int32 m_nBounceLight;
    float32 m_flBounceScale;
    float32 m_flMinRoughness;
    Vector m_vAlternateColor;
    float32 m_fAlternateColorBrightness;
    int32 m_nFog;
    float32 m_flFogStrength;
    int32 m_nFogShadows;
    float32 m_flFogScale;
    bool m_bFogMixedShadows;
    float32 m_flFadeSizeStart;
    float32 m_flFadeSizeEnd;
    float32 m_flShadowFadeSizeStart;
    float32 m_flShadowFadeSizeEnd;
    bool m_bPrecomputedFieldsValid;
    Vector m_vPrecomputedBoundsMins;
    Vector m_vPrecomputedBoundsMaxs;
    Vector m_vPrecomputedOBBOrigin;
    QAngle m_vPrecomputedOBBAngles;
    Vector m_vPrecomputedOBBExtent;
    int32 m_nPrecomputedSubFrusta;
    Vector m_vPrecomputedOBBOrigin0;
    QAngle m_vPrecomputedOBBAngles0;
    Vector m_vPrecomputedOBBExtent0;
    Vector m_vPrecomputedOBBOrigin1;
    QAngle m_vPrecomputedOBBAngles1;
    Vector m_vPrecomputedOBBExtent1;
    Vector m_vPrecomputedOBBOrigin2;
    QAngle m_vPrecomputedOBBAngles2;
    Vector m_vPrecomputedOBBExtent2;
    Vector m_vPrecomputedOBBOrigin3;
    QAngle m_vPrecomputedOBBAngles3;
    Vector m_vPrecomputedOBBExtent3;
    Vector m_vPrecomputedOBBOrigin4;
    QAngle m_vPrecomputedOBBAngles4;
    Vector m_vPrecomputedOBBExtent4;
    Vector m_vPrecomputedOBBOrigin5;
    QAngle m_vPrecomputedOBBAngles5;
    Vector m_vPrecomputedOBBExtent5;
    bool m_bInitialBoneSetup;
    C_NetworkUtlVectorBase< uint16 > m_VisClusters;
};

struct __declspec(align(8)) C_RectLight {
    char m_pad[4208];
    bool m_bShowLight;
};

struct __declspec(align(8)) C_OmniLight {
    char m_pad[4208];
    float32 m_flInnerAngle;
    float32 m_flOuterAngle;
    bool m_bShowLight;
};

struct __declspec(align(8)) C_CSTeam {
    char m_pad[1568];
    char[512] m_szTeamMatchStat;
    int32 m_numMapVictories;
    bool m_bSurrendered;
    int32 m_scoreFirstHalf;
    int32 m_scoreSecondHalf;
    int32 m_scoreOvertime;
    char[129] m_szClanTeamname;
    uint32 m_iClanID;
    char[8] m_szTeamFlagImage;
    char[8] m_szTeamLogoImage;
};

struct __declspec(align(8)) C_MapPreviewParticleSystem {
};

struct __declspec(align(8)) CInfoDynamicShadowHint {
    char m_pad[1384];
    bool m_bDisabled;
    float32 m_flRange;
    int32 m_nImportance;
    int32 m_nLightChoice;
    CHandle< C_BaseEntity > m_hLight;
};

struct __declspec(align(8)) CInfoDynamicShadowHintBox {
    char m_pad[1408];
    Vector m_vBoxMins;
    Vector m_vBoxMaxs;
};

struct __declspec(align(8)) C_EnvSky {
    char m_pad[3368];
    CStrongHandle< InfoForResourceTypeIMaterial2 > m_hSkyMaterial;
    CStrongHandle< InfoForResourceTypeIMaterial2 > m_hSkyMaterialLightingOnly;
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

struct __declspec(align(8)) C_TonemapController2Alias_env_tonemap_controller2 {
};

struct __declspec(align(8)) C_LightEntity {
    char m_pad[3368];
    CLightComponent* m_CLightComponent;
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
    float32 m_flAlphaScale;
    float32 m_flRadiusScale;
    float32 m_flSelfIllumScale;
    Color m_ColorTint;
    CStrongHandle< InfoForResourceTypeCTextureBase > m_hTextureOverride;
};

struct __declspec(align(8)) C_TextureBasedAnimatable {
    char m_pad[3368];
    bool m_bLoop;
    float32 m_flFPS;
    CStrongHandle< InfoForResourceTypeCTextureBase > m_hPositionKeys;
    CStrongHandle< InfoForResourceTypeCTextureBase > m_hRotationKeys;
    Vector m_vAnimationBoundsMin;
    Vector m_vAnimationBoundsMax;
    float32 m_flStartTime;
    float32 m_flStartFrame;
};

struct __declspec(align(8)) C_World {
};

struct __declspec(align(8)) CBaseProp {
    char m_pad[3976];
    bool m_bModelOverrodeBlockLOS;
    int32 m_iShapeType;
    bool m_bConformToCollisionBounds;
    matrix3x4_t m_mPreferredCatchTransform;
};

struct __declspec(align(8)) C_BreakableProp {
    char m_pad[4040];
    CPropDataComponent m_CPropDataComponent;
    CEntityIOOutput m_OnBreak;
    CEntityOutputTemplate< float32 > m_OnHealthChanged;
    CEntityIOOutput m_OnTakeDamage;
    float32 m_impactEnergyScale;
    int32 m_iMinHealthDmg;
    float32 m_flPressureDelay;
    float32 m_flDefBurstScale;
    Vector m_vDefBurstOffset;
    CHandle< C_BaseEntity > m_hBreaker;
    PerformanceMode_t m_PerformanceMode;
    GameTime_t m_flPreventDamageBeforeTime;
    BreakableContentsType_t m_BreakableContentsType;
    CUtlString m_strBreakableContentsPropGroupOverride;
    CUtlString m_strBreakableContentsParticleOverride;
    bool m_bHasBreakPiecesOrCommands;
    float32 m_explodeDamage;
    float32 m_explodeRadius;
    float32 m_explosionDelay;
    CUtlSymbolLarge m_explosionBuildupSound;
    CUtlSymbolLarge m_explosionCustomEffect;
    CUtlSymbolLarge m_explosionCustomSound;
    CUtlSymbolLarge m_explosionModifier;
    CHandle< C_BasePlayerPawn > m_hPhysicsAttacker;
    GameTime_t m_flLastPhysicsInfluenceTime;
    float32 m_flDefaultFadeScale;
    CHandle< C_BaseEntity > m_hLastAttacker;
    CHandle< C_BaseEntity > m_hFlareEnt;
    bool m_noGhostCollision;
};

struct __declspec(align(8)) C_DynamicProp {
    char m_pad[4368];
    bool m_bUseHitboxesForRenderBox;
    bool m_bUseAnimGraph;
    CEntityIOOutput m_pOutputAnimBegun;
    CEntityIOOutput m_pOutputAnimOver;
    CEntityIOOutput m_pOutputAnimLoopCycleOver;
    CEntityIOOutput m_OnAnimReachedStart;
    CEntityIOOutput m_OnAnimReachedEnd;
    CUtlSymbolLarge m_iszIdleAnim;
    AnimLoopMode_t m_nIdleAnimLoopMode;
    bool m_bRandomizeCycle;
    bool m_bStartDisabled;
    bool m_bFiredStartEndOutput;
    bool m_bForceNpcExclude;
    bool m_bCreateNonSolid;
    bool m_bIsOverrideProp;
    int32 m_iInitialGlowState;
    int32 m_nGlowRange;
    int32 m_nGlowRangeMin;
    Color m_glowColor;
    int32 m_nGlowTeam;
    int32 m_iCachedFrameCount;
    Vector m_vecCachedRenderMins;
    Vector m_vecCachedRenderMaxs;
};

struct __declspec(align(8)) C_DynamicPropAlias_dynamic_prop {
};

struct __declspec(align(8)) C_DynamicPropAlias_prop_dynamic_override {
};

struct __declspec(align(8)) C_DynamicPropAlias_cable_dynamic {
};

struct __declspec(align(8)) C_ColorCorrectionVolume {
    char m_pad[3376];
    float32 m_LastEnterWeight;
    float32 m_LastEnterTime;
    float32 m_LastExitWeight;
    float32 m_LastExitTime;
    bool m_bEnabled;
    float32 m_MaxWeight;
    float32 m_FadeDuration;
    float32 m_Weight;
    char[512] m_lookupFilename;
};

struct __declspec(align(16)) C_FuncMonitor {
    char m_pad[3368];
    CUtlString m_targetCamera;
    int32 m_nResolutionEnum;
    bool m_bRenderShadows;
    bool m_bUseUniqueColorTarget;
    CUtlString m_brushModelName;
    CHandle< C_BaseEntity > m_hTargetCamera;
    bool m_bEnabled;
    bool m_bDraw3DSkybox;
};

struct __declspec(align(8)) C_FuncMoveLinear {
};

struct __declspec(align(8)) C_FuncMover {
};

struct __declspec(align(8)) C_PhysMagnet {
    char m_pad[3976];
    CUtlVector< int32 > m_aAttachedObjectsFromServer;
    CUtlVector< CHandle< C_BaseEntity > > m_aAttachedObjects;
};

struct __declspec(align(8)) C_PointCommentaryNode {
    char m_pad[3984];
    bool m_bActive;
    bool m_bWasActive;
    GameTime_t m_flEndTime;
    GameTime_t m_flStartTime;
    float32 m_flStartTimeInCommentary;
    CUtlSymbolLarge m_iszCommentaryFile;
    CUtlSymbolLarge m_iszTitle;
    CUtlSymbolLarge m_iszSpeakers;
    int32 m_iNodeNumber;
    int32 m_iNodeNumberMax;
    bool m_bListenedTo;
    CHandle< C_BaseEntity > m_hViewPosition;
    bool m_bRestartAfterRestore;
};

struct __declspec(align(8)) C_WaterBullet {
};

struct __declspec(align(8)) C_BaseDoor {
    char m_pad[3368];
    bool m_bIsUsable;
};

struct __declspec(align(8)) C_ClientRagdoll {
    char m_pad[3976];
    bool m_bFadeOut;
    bool m_bImportant;
    GameTime_t m_flEffectTime;
    GameTime_t m_gibDespawnTime;
    int32 m_iCurrentFriction;
    int32 m_iMinFriction;
    int32 m_iMaxFriction;
    int32 m_iFrictionAnimState;
    bool m_bReleaseRagdoll;
    AttachmentHandle_t m_iEyeAttachment;
    bool m_bFadingOut;
    float32[10] m_flScaleEnd;
    GameTime_t[10] m_flScaleTimeStart;
    GameTime_t[10] m_flScaleTimeEnd;
};

struct __declspec(align(8)) C_Precipitation {
    char m_pad[3376];
    float32 m_flDensity;
    float32 m_flParticleInnerDist;
    char* m_pParticleDef;
    TimedEvent[1] m_tParticlePrecipTraceTimer;
    bool[1] m_bActiveParticlePrecipEmitter;
    bool m_bParticlePrecipInitialized;
    bool m_bHasSimulatedSinceLastSceneObjectUpdate;
    int32 m_nAvailableSheetSequencesMaxIndex;
};

struct __declspec(align(8)) C_FireSprite {
    char m_pad[3640];
    Vector m_vecMoveDir;
    bool m_bFadeFromAbove;
};

struct __declspec(align(8)) C_FireFromAboveSprite {
};

struct __declspec(align(8)) C_Fish {
    char m_pad[3976];
    Vector m_pos;
    Vector m_vel;
    QAngle m_angles;
    int32 m_localLifeState;
    float32 m_deathDepth;
    float32 m_deathAngle;
    float32 m_buoyancy;
    CountdownTimer m_wiggleTimer;
    float32 m_wigglePhase;
    float32 m_wiggleRate;
    Vector m_actualPos;
    QAngle m_actualAngles;
    Vector m_poolOrigin;
    float32 m_waterLevel;
    bool m_gotUpdate;
    float32 m_x;
    float32 m_y;
    float32 m_z;
    float32 m_angle;
    float32[20] m_errorHistory;
    int32 m_errorHistoryIndex;
    int32 m_errorHistoryCount;
    float32 m_averageError;
};

struct __declspec(align(8)) C_PhysicsProp {
    char m_pad[4368];
    bool m_bAwake;
};

struct __declspec(align(8)) C_BasePropDoor {
    char m_pad[4664];
    DoorState_t m_eDoorState;
    bool m_modelChanged;
    bool m_bLocked;
    Vector m_closedPosition;
    QAngle m_closedAngles;
    CHandle< C_BasePropDoor > m_hMaster;
    Vector m_vWhereToSetLightingOrigin;
};

struct __declspec(align(8)) C_PropDoorRotating {
};

struct __declspec(align(8)) C_PhysPropClientside {
    char m_pad[4368];
    GameTime_t m_flTouchDelta;
    GameTime_t m_fDeathTime;
    float32 m_inertiaScale;
    Vector m_vecDamagePosition;
    Vector m_vecDamageDirection;
    DamageTypes_t m_nDamageType;
};

struct __declspec(align(8)) C_RagdollProp {
    char m_pad[3984];
    C_NetworkUtlVectorBase< Vector > m_ragPos;
    C_NetworkUtlVectorBase< QAngle > m_ragAngles;
    float32 m_flBlendWeight;
    CHandle< C_BaseEntity > m_hRagdollSource;
    AttachmentHandle_t m_iEyeAttachment;
    float32 m_flBlendWeightCurrent;
    CUtlVector< int32 > m_parentPhysicsBoneIndices;
    CUtlVector< int32 > m_worldSpaceBoneComputationOrder;
};

struct __declspec(align(8)) C_LocalTempEntity {
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
    Vector tentOffset;
    QAngle m_vecTempEntAngVelocity;
    int32 tempent_renderamt;
    Vector m_vecNormal;
    float32 m_flSpriteScale;
    int32 m_nFlickerFrame;
    float32 m_flFrameRate;
    float32 m_flFrame;
    char* m_pszImpactEffect;
    char* m_pszParticleEffect;
    bool m_bParticleCollision;
    int32 m_iLastCollisionFrame;
    Vector m_vLastCollisionOrigin;
    Vector m_vecTempEntVelocity;
    Vector m_vecPrevAbsOrigin;
    Vector m_vecTempEntAcceleration;
};

struct __declspec(align(8)) C_ShatterGlassShardPhysics {
    char m_pad[4384];
    shard_model_desc_t m_ShardDesc;
};

struct __declspec(align(8)) C_EconEntity {
    char m_pad[4400];
    float32 m_flFlexDelayTime;
    float32* m_flFlexDelayedWeight;
    bool m_bAttributesInitialized;
    C_AttributeContainer m_AttributeManager;
    uint32 m_OriginalOwnerXuidLow;
    uint32 m_OriginalOwnerXuidHigh;
    int32 m_nFallbackPaintKit;
    int32 m_nFallbackSeed;
    float32 m_flFallbackWear;
    int32 m_nFallbackStatTrak;
    bool m_bClientside;
    bool m_bParticleSystemsCreated;
    CUtlVector< int32 > m_vecAttachedParticles;
    CHandle< CBaseAnimGraph > m_hViewmodelAttachment;
    int32 m_iOldTeam;
    bool m_bAttachmentDirty;
    int32 m_nUnloadedModelIndex;
    int32 m_iNumOwnerValidationRetries;
    CHandle< C_BaseEntity > m_hOldProvidee;
    CUtlVector< C_EconEntity::AttachedModelData_t > m_vecAttachedModels;
};

struct __declspec(align(8)) C_EconWearable {
    char m_pad[5736];
    int32 m_nForceSkin;
    bool m_bAlwaysAllow;
};

struct __declspec(align(8)) C_BaseGrenade {
    char m_pad[4384];
    bool m_bHasWarnedAI;
    bool m_bIsSmokeGrenade;
    bool m_bIsLive;
    float32 m_DmgRadius;
    GameTime_t m_flDetonateTime;
    float32 m_flWarnAITime;
    float32 m_flDamage;
    CUtlSymbolLarge m_iszBounceSound;
    CUtlString m_ExplosionSound;
    CHandle< C_CSPlayerPawn > m_hThrower;
    GameTime_t m_flNextAttack;
    CHandle< C_CSPlayerPawn > m_hOriginalThrower;
};

struct __declspec(align(8)) C_PhysicsPropMultiplayer {
};

struct __declspec(align(8)) C_ViewmodelAttachmentModel {
    char m_pad[3984];
    bool m_bShouldFrontFaceCullLeftHanded;
    bool m_bCreatedLeftHanded;
};

struct __declspec(align(8)) C_PredictedViewModel {
    char m_pad[4080];
    Vector m_vPredictedLagOffset;
    QAngle m_targetSpeed;
    QAngle m_currentSpeed;
};

struct __declspec(align(8)) C_CS2WeaponModuleBase {
};

struct __declspec(align(8)) C_StattrakModule {
    char m_pad[3984];
    bool m_bKnife;
};

struct __declspec(align(8)) C_NametagModule {
    char m_pad[3984];
    CUtlString m_strNametagString;
};

struct __declspec(align(8)) C_KeychainModule {
    char m_pad[3984];
    uint32 m_nKeychainDefID;
    uint32 m_nKeychainSeed;
};

struct __declspec(align(8)) C_BaseCSGrenadeProjectile {
    char m_pad[4464];
    Vector m_vInitialPosition;
    Vector m_vInitialVelocity;
    int32 m_nBounces;
    CStrongHandle< InfoForResourceTypeIParticleSystemDefinition > m_nExplodeEffectIndex;
    int32 m_nExplodeEffectTickBegin;
    Vector m_vecExplodeEffectOrigin;
    GameTime_t m_flSpawnTime;
    Vector vecLastTrailLinePos;
    GameTime_t flNextTrailLineTime;
    bool m_bExplodeEffectBegan;
    bool m_bCanCreateGrenadeTrail;
    ParticleIndex_t m_nSnapshotTrajectoryEffectIndex;
    CStrongHandle< InfoForResourceTypeIParticleSnapshot > m_hSnapshotTrajectoryParticleSnapshot;
    CUtlVector< Vector > m_arrTrajectoryTrailPoints;
    CUtlVector< float32 > m_arrTrajectoryTrailPointCreationTimes;
    float32 m_flTrajectoryTrailEffectCreationTime;
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
    CUtlString m_animgraph;
    CGlobalSymbol m_animgraphCharacterModeString;
    CUtlString m_defaultAnim;
    AnimLoopMode_t m_nDefaultAnimLoopMode;
    float32 m_flInitialModelScale;
    CUtlString m_sInitialWeaponState;
};

struct __declspec(align(8)) C_CSGO_PreviewModelAlias_csgo_item_previewmodel {
};

struct __declspec(align(8)) C_WorldModelGloves {
};

struct __declspec(align(8)) C_BulletHitModel {
    char m_pad[3976];
    matrix3x4_t m_matLocal;
    int32 m_iBoneIndex;
    CHandle< C_BaseEntity > m_hPlayerParent;
    bool m_bIsHit;
    float32 m_flTimeCreated;
    Vector m_vecStartPos;
};

struct __declspec(align(8)) C_HostageCarriableProp {
};

struct __declspec(align(8)) C_PlantedC4 {
    char m_pad[3984];
    bool m_bBombTicking;
    int32 m_nBombSite;
    int32 m_nSourceSoundscapeHash;
    EntitySpottedState_t m_entitySpottedState;
    GameTime_t m_flNextGlow;
    GameTime_t m_flNextBeep;
    GameTime_t m_flC4Blow;
    bool m_bCannotBeDefused;
    bool m_bHasExploded;
    float32 m_flTimerLength;
    bool m_bBeingDefused;
    float32 m_bTriggerWarning;
    float32 m_bExplodeWarning;
    bool m_bC4Activated;
    bool m_bTenSecWarning;
    float32 m_flDefuseLength;
    GameTime_t m_flDefuseCountDown;
    bool m_bBombDefused;
    CHandle< C_CSPlayerPawn > m_hBombDefuser;
    CHandle< C_BaseEntity > m_hControlPanel;
    C_AttributeContainer m_AttributeManager;
    CHandle< C_Multimeter > m_hDefuserMultimeter;
    GameTime_t m_flNextRadarFlashTime;
    bool m_bRadarFlash;
    CHandle< C_CSPlayerPawn > m_pBombDefuser;
    GameTime_t m_fLastDefuseTime;
    CBasePlayerController* m_pPredictionOwner;
    Vector m_vecC4ExplodeSpectatePos;
    QAngle m_vecC4ExplodeSpectateAng;
    float32 m_flC4ExplodeSpectateDuration;
};

struct __declspec(align(8)) C_Multimeter {
    char m_pad[3984];
    CHandle< C_PlantedC4 > m_hTargetC4;
};

struct __declspec(align(8)) C_Item {
    char m_pad[5736];
    char[256] m_pReticleHintTextName;
};

struct __declspec(align(8)) C_HEGrenadeProjectile {
};

struct __declspec(align(8)) C_FlashbangProjectile {
};

struct __declspec(align(8)) C_Chicken {
    char m_pad[4656];
    CHandle< CBaseAnimGraph > m_hHolidayHatAddon;
    bool m_jumpedThisFrame;
    CHandle< C_CSPlayerPawn > m_leader;
    C_AttributeContainer m_AttributeManager;
    bool m_bAttributesInitialized;
    ParticleIndex_t m_hWaterWakeParticles;
    bool m_bIsPreviewModel;
};

struct __declspec(align(8)) C_RagdollPropAttached {
    char m_pad[4096];
    uint32 m_boneIndexAttached;
    uint32 m_ragdollAttachedObjectIndex;
    Vector m_attachmentPointBoneSpace;
    Vector m_attachmentPointRagdollSpace;
    Vector m_vecOffset;
    float32 m_parentTime;
    bool m_bHasParent;
};

struct __declspec(align(8)) C_BaseCombatCharacter {
    char m_pad[4384];
    C_NetworkUtlVectorBase< CHandle< C_EconWearable > > m_hMyWearables;
    AttachmentHandle_t m_leftFootAttachment;
    AttachmentHandle_t m_rightFootAttachment;
    C_BaseCombatCharacter::WaterWakeMode_t m_nWaterWakeMode;
    float32 m_flWaterWorldZ;
    float32 m_flWaterNextTraceTime;
};

struct __declspec(align(8)) C_CSGOViewModel {
    char m_pad[4129];
    bool m_bShouldIgnoreOffsetAndAccuracy;
    CEntityIndex m_nLastKnownAssociatedWeaponEntIndex;
    bool m_bNeedToQueueHighResComposite;
    QAngle m_vLoweredWeaponOffset;
};

struct C_CSWeaponBase {
    char m_pad[5852];
    float32 m_flFireSequenceStartTime;
    int32 m_nFireSequenceStartTimeChange;
    int32 m_nFireSequenceStartTimeAck;
    PlayerAnimEvent_t m_ePlayerFireEvent;
    WeaponAttackType_t m_ePlayerFireEventAttackType;
    HSequence m_seqIdle;
    HSequence m_seqFirePrimary;
    HSequence m_seqFireSecondary;
    CUtlVector< HSequence > m_thirdPersonFireSequences;
    HSequence m_hCurrentThirdPersonSequence;
    int32 m_nSilencerBoneIndex;
    HSequence[7] m_thirdPersonSequences;
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
    bool m_bReloadsWithClips;
    GameTime_t m_flTimeWeaponIdle;
    bool m_bFireOnEmpty;
    CEntityIOOutput m_OnPlayerPickup;
    CSWeaponMode m_weaponMode;
    float32 m_flTurningInaccuracyDelta;
    Vector m_vecTurningInaccuracyEyeDirLast;
    float32 m_flTurningInaccuracy;
    float32 m_fAccuracyPenalty;
    GameTime_t m_flLastAccuracyUpdateTime;
    float32 m_fAccuracySmoothedForZoom;
    GameTime_t m_fScopeZoomEndTime;
    int32 m_iRecoilIndex;
    float32 m_flRecoilIndex;
    bool m_bBurstMode;
    GameTime_t m_flLastBurstModeChangeTime;
    GameTick_t m_nPostponeFireReadyTicks;
    float32 m_flPostponeFireReadyFrac;
    bool m_bInReload;
    bool m_bReloadVisuallyComplete;
    GameTime_t m_flDroppedAtTime;
    bool m_bIsHauledBack;
    bool m_bSilencerOn;
    GameTime_t m_flTimeSilencerSwitchComplete;
    int32 m_iOriginalTeamNumber;
    int32 m_iMostRecentTeamNumber;
    bool m_bDroppedNearBuyZone;
    float32 m_flNextAttackRenderTimeOffset;
    bool m_bClearWeaponIdentifyingUGC;
    bool m_bVisualsDataSet;
    bool m_bOldFirstPersonSpectatedState;
    bool m_bUIWeapon;
    int32 m_nCustomEconReloadEventId;
    CHandle< C_CSPlayerPawn > m_hPrevOwner;
    GameTick_t m_nDropTick;
    bool m_donated;
    GameTime_t m_fLastShotTime;
    bool m_bWasOwnedByCT;
    bool m_bWasOwnedByTerrorist;
    float32 m_gunHeat;
    uint32 m_smokeAttachments;
    GameTime_t m_lastSmokeTime;
    float32 m_flNextClientFireBulletTime;
    float32 m_flNextClientFireBulletTime_Repredict;
    C_IronSightController m_IronSightController;
    int32 m_iIronSightMode;
    GameTime_t m_flLastLOSTraceFailureTime;
    int32 m_iNumEmptyAttacks;
    GameTime_t m_flLastMagDropRequestTime;
    float32 m_flWatTickOffset;
};

struct __declspec(align(16)) C_CSWeaponBaseGun {
    char m_pad[6928];
    int32 m_zoomLevel;
    int32 m_iBurstShotsRemaining;
    int32 m_iSilencerBodygroup;
    int32 m_silencedModelIndex;
    bool m_inPrecache;
    bool m_bNeedsBoltAction;
};

struct __declspec(align(16)) C_C4 {
    char m_pad[6928];
    char[32] m_szScreenText;
    ParticleIndex_t m_activeLightParticleIndex;
    C4LightEffect_t m_eActiveLightEffect;
    bool m_bStartedArming;
    GameTime_t m_fArmedTime;
    bool m_bBombPlacedAnimation;
    bool m_bIsPlantingViaUse;
    EntitySpottedState_t m_entitySpottedState;
    int32 m_nSpotRules;
    bool[7] m_bPlayedArmingBeeps;
    bool m_bBombPlanted;
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
    GameTime_t m_fFireTime;
    int32 m_nLastAttackTick;
};

struct __declspec(align(16)) C_WeaponXM1014 {
};

struct __declspec(align(16)) C_Knife {
};

struct __declspec(align(16)) C_Melee {
};

struct __declspec(align(16)) C_WeaponShield {
    char m_pad[6960];
    float32 m_flDisplayHealth;
};

struct __declspec(align(8)) C_MolotovProjectile {
    char m_pad[4616];
    bool m_bIsIncGrenade;
};

struct __declspec(align(8)) C_DecoyProjectile {
    char m_pad[4616];
    int32 m_nDecoyShotTick;
    int32 m_nClientLastKnownDecoyShotTick;
    GameTime_t m_flTimeParticleEffectSpawn;
};

struct __declspec(align(8)) C_SmokeGrenadeProjectile {
    char m_pad[4624];
    int32 m_nSmokeEffectTickBegin;
    bool m_bDidSmokeEffect;
    int32 m_nRandomSeed;
    Vector m_vSmokeColor;
    Vector m_vSmokeDetonationPos;
    CUtlVector< uint8 > m_VoxelFrameData;
    bool m_bSmokeVolumeDataReceived;
    bool m_bSmokeEffectSpawned;
};

struct C_BaseCSGrenade {
    char m_pad[6928];
    bool m_bClientPredictDelete;
    bool m_bRedraw;
    bool m_bIsHeldByPlayer;
    bool m_bPinPulled;
    bool m_bJumpThrow;
    bool m_bThrowAnimating;
    GameTime_t m_fThrowTime;
    float32 m_flThrowStrength;
    float32 m_flThrowStrengthApproach;
    GameTime_t m_fDropTime;
    GameTime_t m_fPinPullTime;
    bool m_bJustPulledPin;
    GameTick_t m_nNextHoldTick;
    float32 m_flNextHoldFrac;
    CHandle< C_CSWeaponBase > m_hSwitchToWeaponAfterThrow;
};

struct C_WeaponBaseItem {
    char m_pad[6928];
    CountdownTimer m_SequenceCompleteTimer;
    bool m_bRedraw;
};

struct __declspec(align(8)) C_ItemDogtags {
    char m_pad[5992];
    CHandle< C_CSPlayerPawn > m_OwningPlayer;
    CHandle< C_CSPlayerPawn > m_KillingPlayer;
};

struct __declspec(align(16)) C_Item_Healthshot {
};

struct __declspec(align(16)) C_Fists {
    char m_pad[6928];
    bool m_bPlayingUninterruptableAct;
    PlayerAnimEvent_t m_nUninterruptableActivity;
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
    CCSPlayer_PingServices* m_pPingServices;
    CPlayer_ViewModelServices* m_pViewModelServices;
    float32[4] m_fRenderingClipPlane;
    int32 m_nLastClipPlaneSetupFrame;
    Vector m_vecLastClipCameraPos;
    Vector m_vecLastClipCameraForward;
    bool m_bClipHitStaticWorld;
    bool m_bCachedPlaneIsValid;
    C_CSWeaponBase* m_pClippingWeapon;
    CSPlayerState m_previousPlayerState;
    CSPlayerState m_iPlayerState;
    bool m_bIsRescuing;
    GameTime_t m_fImmuneToGunGameDamageTime;
    GameTime_t m_fImmuneToGunGameDamageTimeLast;
    bool m_bGunGameImmunity;
    bool m_bHasMovedSinceSpawn;
    float32 m_fMolotovUseTime;
    float32 m_fMolotovDamageTime;
    int32 m_iThrowGrenadeCounter;
    GameTime_t m_flLastSpawnTimeIndex;
    int32 m_iProgressBarDuration;
    float32 m_flProgressBarStartTime;
    Vector m_vecIntroStartEyePosition;
    Vector m_vecIntroStartPlayerForward;
    GameTime_t m_flClientDeathTime;
    bool m_bScreenTearFrameCaptured;
    float32 m_flFlashBangTime;
    float32 m_flFlashScreenshotAlpha;
    float32 m_flFlashOverlayAlpha;
    bool m_bFlashBuildUp;
    bool m_bFlashDspHasBeenCleared;
    bool m_bFlashScreenshotHasBeenGrabbed;
    float32 m_flFlashMaxAlpha;
    float32 m_flFlashDuration;
    int32 m_iHealthBarRenderMaskIndex;
    float32 m_flHealthFadeValue;
    float32 m_flHealthFadeAlpha;
    float32 m_flDeathCCWeight;
    float32 m_flPrevRoundEndTime;
    float32 m_flPrevMatchEndTime;
    QAngle m_angEyeAngles;
    float32 m_fNextThinkPushAway;
    bool m_bShouldAutobuyDMWeapons;
    bool m_bShouldAutobuyNow;
    CEntityIndex m_iIDEntIndex;
    CountdownTimer m_delayTargetIDTimer;
    CEntityIndex m_iTargetItemEntIdx;
    CEntityIndex m_iOldIDEntIndex;
    CountdownTimer m_holdTargetIDTimer;
    float32 m_flCurrentMusicStartTime;
    float32 m_flMusicRoundStartTime;
    bool m_bDeferStartMusicOnWarmup;
    int32 m_cycleLatch;
    float32 m_serverIntendedCycle;
    float32 m_flLastSmokeOverlayAlpha;
    float32 m_flLastSmokeAge;
    Vector m_vLastSmokeOverlayColor;
    ParticleIndex_t m_nPlayerSmokedFx;
    ParticleIndex_t m_nPlayerInfernoBodyFx;
    ParticleIndex_t m_nPlayerInfernoFootFx;
    float32 m_flNextMagDropTime;
    int32 m_nLastMagDropAttachmentIndex;
    Vector m_vecLastAliveLocalVelocity;
    bool m_bGuardianShouldSprayCustomXMark;
    CHandle< CCSPlayerController > m_hOriginalController;
};

struct __declspec(align(8)) C_Hostage {
    char m_pad[4520];
    EntitySpottedState_t m_entitySpottedState;
    CHandle< C_BaseEntity > m_leader;
    CountdownTimer m_reuseTimer;
    Vector m_vel;
    bool m_isRescued;
    bool m_jumpedThisFrame;
    int32 m_nHostageState;
    bool m_bHandsHaveBeenCut;
    CHandle< C_CSPlayerPawn > m_hHostageGrabber;
    GameTime_t m_fLastGrabTime;
    Vector m_vecGrabbedPos;
    GameTime_t m_flRescueStartTime;
    GameTime_t m_flGrabSuccessTime;
    GameTime_t m_flDropStartTime;
    GameTime_t m_flDeadOrRescuedTime;
    CountdownTimer m_blinkTimer;
    Vector m_lookAt;
    CountdownTimer m_lookAroundTimer;
    bool m_isInit;
    AttachmentHandle_t m_eyeAttachment;
    AttachmentHandle_t m_chestAttachment;
    CBasePlayerController* m_pPredictionOwner;
    GameTime_t m_fNewestAlphaThinkTime;
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
    CUtlString m_animgraph;
    CGlobalSymbol m_animgraphCharacterModeString;
    float32 m_flInitialModelScale;
};

struct __declspec(align(16)) C_CSGO_PreviewPlayerAlias_csgo_player_previewmodel {
};

