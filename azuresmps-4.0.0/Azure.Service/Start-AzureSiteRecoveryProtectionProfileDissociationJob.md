---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 185506BC-6155-4517-BCBD-BCDE7450C7A8
online version: ''
schema: 2.0.0
ms.openlocfilehash: f8017c2947a8d046226a63b5ed07b3714c35b22c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106410"
---
# <span data-ttu-id="fa96e-101">Start-AzureSiteRecoveryProtectionProfileDissociationJob</span><span class="sxs-lookup"><span data-stu-id="fa96e-101">Start-AzureSiteRecoveryProtectionProfileDissociationJob</span></span>

## <span data-ttu-id="fa96e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa96e-102">SYNOPSIS</span></span>
<span data-ttu-id="fa96e-103">Site kurtarma koruma konteyneriyle ilişkilendirilmiş bir çoğaltma ilkesinde ilişkilendirme işini başlatır.</span><span class="sxs-lookup"><span data-stu-id="fa96e-103">Starts a dissociation job on a replication policy associated with a Site Recovery protection container.</span></span>

## <span data-ttu-id="fa96e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fa96e-104">SYNTAX</span></span>

### <span data-ttu-id="fa96e-105">EnterpriseToAzure (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="fa96e-105">EnterpriseToAzure (Default)</span></span>
```
Start-AzureSiteRecoveryProtectionProfileDissociationJob -ProtectionProfile <ASRProtectionProfile>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="fa96e-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="fa96e-106">EnterpriseToEnterprise</span></span>
```
Start-AzureSiteRecoveryProtectionProfileDissociationJob -ProtectionProfile <ASRProtectionProfile>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="fa96e-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="fa96e-107">DESCRIPTION</span></span>
<span data-ttu-id="fa96e-108">**Start-AzureSiteRecoveryProtectionProfileDissociationJob** cmdlet 'ı, Azure Site Recovery koruma kapsayıcısı ile ilişkilendirilen çoğaltma ilkesinde bir ilişkilendirme işi başlatır.</span><span class="sxs-lookup"><span data-stu-id="fa96e-108">The **Start-AzureSiteRecoveryProtectionProfileDissociationJob** cmdlet initiates a dissociation job on the replication policy associated with an Azure Site Recovery protection container.</span></span>

## <span data-ttu-id="fa96e-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fa96e-109">EXAMPLES</span></span>

### <span data-ttu-id="fa96e-110">Örnek 1: koruma profilini ayırma</span><span class="sxs-lookup"><span data-stu-id="fa96e-110">Example 1: Dissociate a protection profile</span></span>
```
PS C:\> $ProtectionContainer01 = Get-AzureSiteRecoveryProtectionContainer -Id "5ba2ea95-856d-4033-9ca3-91e3e2c080b9"
PS C:\> $ProtectionContainer02 = Get-AzureSiteRecoveryProtectionContainer -Id "cf011f2a-aa19-443c-9f60-357f6b8afb77"
PS C:\> Start-AzureSiteRecoveryProtectionProfileDissociationJob -PrimaryProtectionContainer $ProtectionContainer01 -ProtectionProfile $ProtectionContainer01.AvailableProtectionProfiles[0] -RecoveryProtectionContainer $ProtectionContainer02
Name             : MyProtectionProfile
ID               : 51978b0f-9241-4153-9171-2e19344f0805
ClientRequestId  : bb6f3200-b7c6-4c6f-bcbc-a70bb9946f03-2015-01-30 02:55:55Z-P
State            : NotStarted
StateDescription : NotStarted
StartTime        : 
EndTime          : 
AllowedActions   : 
Tasks            : {}
Errors           : {}
```

<span data-ttu-id="fa96e-111">İlk komut **Get-AzureSiteRecoveryProtectionContainer** cmdlet 'ini kullanarak bir koruma kapsayıcısı alır ve bu kapsayıcıyı $ProtectionContainer 01 değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="fa96e-111">The first command gets a protection container by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores that container in the $ProtectionContainer01 variable.</span></span>

<span data-ttu-id="fa96e-112">İkinci komut bir koruma kapsayıcısı alır ve $ProtectionContainer 02 değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="fa96e-112">The second command gets a protection container, and then stores it in the $ProtectionContainer02 variable.</span></span>

<span data-ttu-id="fa96e-113">Son komut, $ProtectionContainer 01 ' de depolanan kapsayıcıdaki koruma profilinin birincil koruma kapsayıcısı olarak ilişkisini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="fa96e-113">The final command dissociates the protection profile from the container stored in $ProtectionContainer01 as the primary protection container.</span></span>
<span data-ttu-id="fa96e-114">Komut, $ProtectionContainer 02 ' de depolanan kapsayıcıyı kurtarma koruma kapsayıcısı olarak ayırtır.</span><span class="sxs-lookup"><span data-stu-id="fa96e-114">The command dissociates the container stored in $ProtectionContainer02 as the recovery protection container.</span></span>

## <span data-ttu-id="fa96e-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fa96e-115">PARAMETERS</span></span>

### <span data-ttu-id="fa96e-116">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="fa96e-116">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="fa96e-117">Birincil koruma kapsayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fa96e-117">Specifies a primary protection container.</span></span>

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

### <span data-ttu-id="fa96e-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="fa96e-118">-Profile</span></span>
<span data-ttu-id="fa96e-119">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fa96e-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fa96e-120">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="fa96e-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="fa96e-121">-ProtectionProfile</span><span class="sxs-lookup"><span data-stu-id="fa96e-121">-ProtectionProfile</span></span>
<span data-ttu-id="fa96e-122">Koruma kapsayıcılarından, koruma kapsayıcılarının ilişkisini belirler.</span><span class="sxs-lookup"><span data-stu-id="fa96e-122">Specifies the protection profile settings to disassociate from the protection containers.</span></span>
<span data-ttu-id="fa96e-123">Koruma kapsayıcılarına uygulanacak koruma profili ayarlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fa96e-123">Specifies the protection profile settings to apply to the protection containers.</span></span>
<span data-ttu-id="fa96e-124">Bir **Asrprotectionprofile** nesnesi edinmek için New-AzureSiteRecoveryProtectionProfileObject cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="fa96e-124">To obtain an **ASRProtectionProfile** object, use the New-AzureSiteRecoveryProtectionProfileObject cmdlet.</span></span>

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

### <span data-ttu-id="fa96e-125">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="fa96e-125">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="fa96e-126">Kurtarma koruma kapsayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fa96e-126">Specifies a recovery protection container.</span></span>

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

### <span data-ttu-id="fa96e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa96e-127">CommonParameters</span></span>
<span data-ttu-id="fa96e-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fa96e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa96e-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa96e-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa96e-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fa96e-130">INPUTS</span></span>

## <span data-ttu-id="fa96e-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fa96e-131">OUTPUTS</span></span>

## <span data-ttu-id="fa96e-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fa96e-132">NOTES</span></span>

## <span data-ttu-id="fa96e-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fa96e-133">RELATED LINKS</span></span>

[<span data-ttu-id="fa96e-134">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="fa96e-134">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="fa96e-135">New-AzureSiteRecoveryProtectionProfileObject</span><span class="sxs-lookup"><span data-stu-id="fa96e-135">New-AzureSiteRecoveryProtectionProfileObject</span></span>](./New-AzureSiteRecoveryProtectionProfileObject.md)

[<span data-ttu-id="fa96e-136">Start-AzureSiteRecoveryProtectionProfileAssociationJob</span><span class="sxs-lookup"><span data-stu-id="fa96e-136">Start-AzureSiteRecoveryProtectionProfileAssociationJob</span></span>](./Start-AzureSiteRecoveryProtectionProfileAssociationJob.md)


