---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: CB5E1419-C4C7-4524-ACCC-13C9D9CCA621
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4955bfa121d6742903dd2ca99721186c7c860004
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105848"
---
# <span data-ttu-id="6676f-101">Start-AzureSiteRecoveryProtectionProfileAssociationJob</span><span class="sxs-lookup"><span data-stu-id="6676f-101">Start-AzureSiteRecoveryProtectionProfileAssociationJob</span></span>

## <span data-ttu-id="6676f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6676f-102">SYNOPSIS</span></span>
<span data-ttu-id="6676f-103">Site kurtarma çoğaltması ilkesi ilişki işini başlatır.</span><span class="sxs-lookup"><span data-stu-id="6676f-103">Starts a Site Recovery replication policy association job.</span></span>

## <span data-ttu-id="6676f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6676f-104">SYNTAX</span></span>

### <span data-ttu-id="6676f-105">EnterpriseToAzure (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6676f-105">EnterpriseToAzure (Default)</span></span>
```
Start-AzureSiteRecoveryProtectionProfileAssociationJob -ProtectionProfile <ASRProtectionProfile>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="6676f-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="6676f-106">EnterpriseToEnterprise</span></span>
```
Start-AzureSiteRecoveryProtectionProfileAssociationJob -ProtectionProfile <ASRProtectionProfile>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="6676f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="6676f-107">DESCRIPTION</span></span>
<span data-ttu-id="6676f-108">**Start-AzureSiteRecoveryProtectionProfileAssociationJob** cmdlet 'i bir çoğaltma Ilkesini Azure Site Recovery koruma konteyneriyle ilişkilendirmek için bir ilişkilendirme işi başlatır.</span><span class="sxs-lookup"><span data-stu-id="6676f-108">The **Start-AzureSiteRecoveryProtectionProfileAssociationJob** cmdlet initiates an association job to associate a replication policy with an Azure Site Recovery protection container.</span></span>

## <span data-ttu-id="6676f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6676f-109">EXAMPLES</span></span>

### <span data-ttu-id="6676f-110">Örnek 1: koruma profilini Ilişkilendirme</span><span class="sxs-lookup"><span data-stu-id="6676f-110">Example 1: Associate a protection profile</span></span>
```
PS C:\> $ProtectionContainer01 = Get-AzureSiteRecoveryProtectionContainer -Id "5ba2ea95-856d-4033-9ca3-91e3e2c080b9"
PS C:\> $ProtectionProfile = New-AzureSiteRecoveryProtectionProfileObject -ReplicationProvider "HyperVReplica" -AllowReplicaDeletion -ApplicationConsistentSnapshotFrequencyInHours 1 -CompressionEnabled -RecoveryPoints 2 -ReplicationFrequencyInSeconds 30 -ReplicationMethod "Online" -ReplicationPort 8085 -ReplicationStartTime 1
PS C:\> $ProtectionContainer02 = Get-AzureSiteRecoveryProtectionContainer -Id "cf011f2a-aa19-443c-9f60-357f6b8afb77"
PS C:\> Start-AzureSiteRecoveryProtectionProfileAssociationJob -PrimaryProtectionContainer $ProtectionContainer01 -ProtectionProfile $ProtectionProfile -RecoveryProtectionContainer $ProtectionContainer02
Name             : MyProtectionProfile
ID               : 51978b0f-9241-4153-9171-2e19344f0805
ClientRequestId  : bb6f3200-b7c6-4c6f-bcbc-a70bb9946f03-2015-01-27 22:55:55Z-P
State            : InProgress
StateDescription : InProgress
StartTime        : 1/27/2015 10:56:01 PM
EndTime          : 
AllowedActions   : 
Tasks            : {Adding the protection group, Configuring Windows Server 2012 R2 Hyper-V hosts for Azure}
Errors           : {}
```

<span data-ttu-id="6676f-111">İlk komut **Get-AzureSiteRecoveryProtectionContainer** cmdlet 'ini kullanarak bir koruma kapsayıcısı alır ve bu kapsayıcıyı $ProtectionContainer 01 değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="6676f-111">The first command gets a protection container by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores that container in the $ProtectionContainer01 variable.</span></span>

<span data-ttu-id="6676f-112">İkinci komut, **New-AzureSiteRecoveryProtectionProfileObject** cmdlet 'ini kullanarak bir koruma profili oluşturur ve bu koruma profilini $ProtectionProfile değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="6676f-112">The second command creates a protection profile by using the **New-AzureSiteRecoveryProtectionProfileObject** cmdlet, and stores that protection profile in the $ProtectionProfile variable.</span></span>

<span data-ttu-id="6676f-113">Üçüncü komut bir koruma kapsayıcısı alır ve $ProtectionContainer 02 değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="6676f-113">The third command gets a protection container, and then stores it in the $ProtectionContainer02 variable.</span></span>

<span data-ttu-id="6676f-114">Son komutu $ProtectionProfile 'da depolanan koruma profilini, $ProtectionContainer 01 ' de depolanan kapsayıcıya birincil koruma kapsayıcısı olarak ilişkilendirir.</span><span class="sxs-lookup"><span data-stu-id="6676f-114">The final command associates the protection profile stored in $ProtectionProfile to the container stored in $ProtectionContainer01 as the primary protection container.</span></span>
<span data-ttu-id="6676f-115">Komut $ProtectionContainer 02 ' de depolanan kapsayıcıyı kurtarma koruma kapsayıcısı olarak ilişkilendirir.</span><span class="sxs-lookup"><span data-stu-id="6676f-115">The command associates the container stored in $ProtectionContainer02 as the recovery protection container.</span></span>

## <span data-ttu-id="6676f-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6676f-116">PARAMETERS</span></span>

### <span data-ttu-id="6676f-117">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="6676f-117">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="6676f-118">Koruma profili ayarlarının uygulanacağı birincil koruma kapsayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6676f-118">Specifies the primary protection container on which to apply the protection profile settings.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6676f-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="6676f-119">-Profile</span></span>
<span data-ttu-id="6676f-120">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6676f-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6676f-121">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="6676f-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6676f-122">-ProtectionProfile</span><span class="sxs-lookup"><span data-stu-id="6676f-122">-ProtectionProfile</span></span>
<span data-ttu-id="6676f-123">Koruma kapsayıcılarına uygulanacak koruma profili ayarlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6676f-123">Specifies the protection profile settings to apply to the protection containers.</span></span>
<span data-ttu-id="6676f-124">Bir **Asrprotectionprofile** nesnesi edinmek için New-AzureSiteRecoveryProtectionProfileObject cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="6676f-124">To obtain an **ASRProtectionProfile** object, use the New-AzureSiteRecoveryProtectionProfileObject cmdlet.</span></span>

```yaml
Type: ASRProtectionProfile
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6676f-125">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="6676f-125">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="6676f-126">Koruma profili ayarlarının uygulanacağı kurtarma koruması kapsayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6676f-126">Specifies the recovery protection container on which to apply the protection profile settings.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6676f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6676f-127">CommonParameters</span></span>
<span data-ttu-id="6676f-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6676f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6676f-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6676f-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6676f-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6676f-130">INPUTS</span></span>

## <span data-ttu-id="6676f-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6676f-131">OUTPUTS</span></span>

## <span data-ttu-id="6676f-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6676f-132">NOTES</span></span>

## <span data-ttu-id="6676f-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6676f-133">RELATED LINKS</span></span>

[<span data-ttu-id="6676f-134">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="6676f-134">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="6676f-135">New-AzureSiteRecoveryProtectionProfileObject</span><span class="sxs-lookup"><span data-stu-id="6676f-135">New-AzureSiteRecoveryProtectionProfileObject</span></span>](./New-AzureSiteRecoveryProtectionProfileObject.md)

[<span data-ttu-id="6676f-136">Start-AzureSiteRecoveryProtectionProfileDissociationJob</span><span class="sxs-lookup"><span data-stu-id="6676f-136">Start-AzureSiteRecoveryProtectionProfileDissociationJob</span></span>](./Start-AzureSiteRecoveryProtectionProfileDissociationJob.md)


