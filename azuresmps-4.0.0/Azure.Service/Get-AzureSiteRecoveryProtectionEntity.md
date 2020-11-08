---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: CB1A36E9-75BE-43CF-9092-9713DFEB96F8
online version: ''
schema: 2.0.0
ms.openlocfilehash: d5329d50f87b92254136c222f406bb49586d6d7a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105588"
---
# <span data-ttu-id="453f2-101">Get-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="453f2-101">Get-AzureSiteRecoveryProtectionEntity</span></span>

## <span data-ttu-id="453f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="453f2-102">SYNOPSIS</span></span>
<span data-ttu-id="453f2-103">Bir site kurtarma kasasındaki korunabilir veya korunmuş varlıklar alır.</span><span class="sxs-lookup"><span data-stu-id="453f2-103">Gets protectable or protected entities in a Site Recovery vault.</span></span>

## <span data-ttu-id="453f2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="453f2-104">SYNTAX</span></span>

### <span data-ttu-id="453f2-105">ByObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="453f2-105">ByObject (Default)</span></span>
```
Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer <ASRProtectionContainer> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="453f2-106">ByObjectWithId</span><span class="sxs-lookup"><span data-stu-id="453f2-106">ByObjectWithId</span></span>
```
Get-AzureSiteRecoveryProtectionEntity -Id <String> -ProtectionContainer <ASRProtectionContainer>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="453f2-107">Byidswithıd</span><span class="sxs-lookup"><span data-stu-id="453f2-107">ByIDsWithId</span></span>
```
Get-AzureSiteRecoveryProtectionEntity -Id <String> -ProtectionContainerId <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="453f2-108">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="453f2-108">ByObjectWithName</span></span>
```
Get-AzureSiteRecoveryProtectionEntity -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="453f2-109">ByIDsWithName</span><span class="sxs-lookup"><span data-stu-id="453f2-109">ByIDsWithName</span></span>
```
Get-AzureSiteRecoveryProtectionEntity -Name <String> -ProtectionContainerId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="453f2-110">Kimlikler</span><span class="sxs-lookup"><span data-stu-id="453f2-110">ByIDs</span></span>
```
Get-AzureSiteRecoveryProtectionEntity -ProtectionContainerId <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="453f2-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="453f2-111">DESCRIPTION</span></span>
<span data-ttu-id="453f2-112">**Get-AzureSiteRecoveryProtectionEntity** cmdlet 'ı geçerli Azure Site Recovery kasasındaki sanal makineler gibi korumalı varlıkları veya korumalı varlıkları alır.</span><span class="sxs-lookup"><span data-stu-id="453f2-112">The **Get-AzureSiteRecoveryProtectionEntity** cmdlet gets the protectable or protected entities, such as virtual machines, in the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="453f2-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="453f2-113">EXAMPLES</span></span>

### <span data-ttu-id="453f2-114">Örnek 1: kapsayıcıda korumalı bir sanal makine görüntüleme</span><span class="sxs-lookup"><span data-stu-id="453f2-114">Example 1: Display a protected virtual machine in a container</span></span>
```
PS C:\> $Container = Get-AzureSiteRecoveryProtectionContainer
PS C:\> Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $Container 
ID                           : 43aaab46-1cb0-4c39-8077-9a091c3b05ce
ServerId                     : 4a94c4a9-c856-4577-afbd-367fe9b3ce9c
ProtectionContainerId        : 4a94c4a9-c856-4577-afbd-367fe9b3ce9c_1c513d45-645d-4ed0-b9ae-e7b869a1f7fc
Name                         : testvm
Type                         : VirtualMachine
FabricObjectId               : 506B3CAC-5758-49E2-98C4-E5B0512E4D8E
Protected                    : False
CanCommit                    : False
CanFailover                  : False
CanReverseReplicate          : False
ActiveLocation               : Primary
ProtectionStateDescription   : Enabling protection
ReplicationHealth            : 
TestFailoverStateDescription : Nonev
ReplicationProvider          : HyperVReplica
```

<span data-ttu-id="453f2-115">İlk komut **Get-AzureSiteRecoveryProtectionContainer** cmdlet 'ini kullanarak korumalı bir kapsayıcı alır ve bu nesneyi $Container değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="453f2-115">The first command gets a protected container by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores that object in the $Container variable.</span></span>

<span data-ttu-id="453f2-116">İkinci komut, $Container kapsayıcıya ait korumalı sanal makineyi alır ve ardından görüntüler.</span><span class="sxs-lookup"><span data-stu-id="453f2-116">The second command gets the protected virtual machine that belongs to the container in $Container, and then displays it.</span></span>

## <span data-ttu-id="453f2-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="453f2-117">PARAMETERS</span></span>

### <span data-ttu-id="453f2-118">-ID</span><span class="sxs-lookup"><span data-stu-id="453f2-118">-Id</span></span>
<span data-ttu-id="453f2-119">Alınacak bir koruma varlığının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="453f2-119">Specifies the ID of a protection entity to get.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithId, ByIDsWithId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="453f2-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="453f2-120">-Name</span></span>
<span data-ttu-id="453f2-121">Alınacak koruma varlığının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="453f2-121">Specifies the name of a protection entity to get.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithName, ByIDsWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="453f2-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="453f2-122">-Profile</span></span>
<span data-ttu-id="453f2-123">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="453f2-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="453f2-124">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="453f2-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="453f2-125">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="453f2-125">-ProtectionContainer</span></span>
<span data-ttu-id="453f2-126">Bir koruma kapsayıcısı belirtir.</span><span class="sxs-lookup"><span data-stu-id="453f2-126">Specifies a protection container.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: ASRProtectionContainer
Parameter Sets: ByObjectWithId, ByObjectWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="453f2-127">-Protectioncontainerıd</span><span class="sxs-lookup"><span data-stu-id="453f2-127">-ProtectionContainerId</span></span>
<span data-ttu-id="453f2-128">Korumalı bir kapsayıcının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="453f2-128">Specifies the ID of a protected container.</span></span>

```yaml
Type: String
Parameter Sets: ByIDsWithId, ByIDsWithName, ByIDs
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="453f2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="453f2-129">CommonParameters</span></span>
<span data-ttu-id="453f2-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="453f2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="453f2-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="453f2-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="453f2-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="453f2-132">INPUTS</span></span>

## <span data-ttu-id="453f2-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="453f2-133">OUTPUTS</span></span>

## <span data-ttu-id="453f2-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="453f2-134">NOTES</span></span>

## <span data-ttu-id="453f2-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="453f2-135">RELATED LINKS</span></span>

[<span data-ttu-id="453f2-136">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="453f2-136">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="453f2-137">Set-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="453f2-137">Set-AzureSiteRecoveryProtectionEntity</span></span>](./Set-AzureSiteRecoveryProtectionEntity.md)

[<span data-ttu-id="453f2-138">Güncelleştirme-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="453f2-138">Update-AzureSiteRecoveryProtectionEntity</span></span>](./Update-AzureSiteRecoveryProtectionEntity.md)


