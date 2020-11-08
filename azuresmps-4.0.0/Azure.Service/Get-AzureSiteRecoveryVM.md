---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: CE15E01D-5D86-4960-8E37-7757B35F4464
online version: ''
schema: 2.0.0
ms.openlocfilehash: a87a825249d7d7cda3fc2dc43a93869f8d869705
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106569"
---
# <span data-ttu-id="efee2-101">Get-AzureSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="efee2-101">Get-AzureSiteRecoveryVM</span></span>

## <span data-ttu-id="efee2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="efee2-102">SYNOPSIS</span></span>
<span data-ttu-id="efee2-103">Site kurtarma ile yönetilen sanal makineler hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="efee2-103">Gets information about Site Recovery-managed virtual machines.</span></span>

## <span data-ttu-id="efee2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="efee2-104">SYNTAX</span></span>

### <span data-ttu-id="efee2-105">ByObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="efee2-105">ByObject (Default)</span></span>
```
Get-AzureSiteRecoveryVM -ProtectionContainer <ASRProtectionContainer> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="efee2-106">ByObjectWithId</span><span class="sxs-lookup"><span data-stu-id="efee2-106">ByObjectWithId</span></span>
```
Get-AzureSiteRecoveryVM -Id <String> -ProtectionContainer <ASRProtectionContainer> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="efee2-107">Byidswithıd</span><span class="sxs-lookup"><span data-stu-id="efee2-107">ByIDsWithId</span></span>
```
Get-AzureSiteRecoveryVM -Id <String> -ProtectionContainerId <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="efee2-108">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="efee2-108">ByObjectWithName</span></span>
```
Get-AzureSiteRecoveryVM -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="efee2-109">ByIDsWithName</span><span class="sxs-lookup"><span data-stu-id="efee2-109">ByIDsWithName</span></span>
```
Get-AzureSiteRecoveryVM -Name <String> -ProtectionContainerId <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="efee2-110">Kimlikler</span><span class="sxs-lookup"><span data-stu-id="efee2-110">ByIDs</span></span>
```
Get-AzureSiteRecoveryVM -ProtectionContainerId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="efee2-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="efee2-111">DESCRIPTION</span></span>
<span data-ttu-id="efee2-112">**Get-AzureSiteRecoveryVM** cmdlet 'ı Azure Site Recovery 'de yönetilen sanal makineler hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="efee2-112">The **Get-AzureSiteRecoveryVM** cmdlet gets information about virtual machines managed in Azure Site Recovery.</span></span>

## <span data-ttu-id="efee2-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="efee2-113">EXAMPLES</span></span>

### <span data-ttu-id="efee2-114">Örnek 1: sanal makine hakkında bilgi alma</span><span class="sxs-lookup"><span data-stu-id="efee2-114">Example 1: Get information about a virtual machine</span></span>
```
PS C:\> $ProtectionContainer = Get-AzureSiteRecoveryProtectionContainer
PS C:\> Get-AzureSiteRecoveryVM -ProtectionContainer $ProtectionContainer
ID                          : a205fd17-3848-4896-bab6-9dbccc3cd8ed
ServerId                    : 4a94c4a9-c856-4577-afbd-367fe9b3ce9c
ProtectionContainerId       : 4a94c4a9-c856-4577-afbd-367fe9b3ce9c_1c513d45-645d-4ed0-b9ae-e7b869a1f7fc
Name                        : vm1
Type                        : VirtualMachine
FabricObjectId              : 86447b9e-d877-4e9a-8302-adcd6bbf18c0
Protected                   : False
CanCommit                   : False
CanFailover                 : True
CanReverseReplicate         : False
ActiveLocation              : Primary
ProtectionState             : Enabled
ReplicationHealth           : Healthy
TestFailoverState           : None
ReplicationProvider         : HyperVReplica
```

<span data-ttu-id="efee2-115">İlk komut, korumalı bir kapsayıcı almak için **Get-AzureSiteRecoveryProtectionContainer** cmdlet 'ini kullanır ve ardından $ProtectionContainer değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="efee2-115">The first command uses the **Get-AzureSiteRecoveryProtectionContainer** cmdlet to get a protected container, and then stores it in the $ProtectionContainer variable.</span></span>

<span data-ttu-id="efee2-116">İkinci komut $ProtectionContainer sanal makinelerle ilgili bilgileri alır.</span><span class="sxs-lookup"><span data-stu-id="efee2-116">The second command gets information about the virtual machines in $ProtectionContainer.</span></span>

## <span data-ttu-id="efee2-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="efee2-117">PARAMETERS</span></span>

### <span data-ttu-id="efee2-118">-ID</span><span class="sxs-lookup"><span data-stu-id="efee2-118">-Id</span></span>
<span data-ttu-id="efee2-119">Bilgi alınacak sanal makinenin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="efee2-119">Specifies the ID of the virtual machine about which to get information.</span></span>

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

### <span data-ttu-id="efee2-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="efee2-120">-Name</span></span>
<span data-ttu-id="efee2-121">Sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="efee2-121">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="efee2-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="efee2-122">-Profile</span></span>
<span data-ttu-id="efee2-123">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="efee2-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="efee2-124">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="efee2-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="efee2-125">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="efee2-125">-ProtectionContainer</span></span>
<span data-ttu-id="efee2-126">Site Recovery koruması kapsayıcı nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="efee2-126">Specifies the Site Recovery protection container object.</span></span>

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

### <span data-ttu-id="efee2-127">-Protectioncontainerıd</span><span class="sxs-lookup"><span data-stu-id="efee2-127">-ProtectionContainerId</span></span>
<span data-ttu-id="efee2-128">Bilgi alınacak korumalı kapsayıcının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="efee2-128">Specifies the ID of a protected container about which to get information.</span></span>

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

### <span data-ttu-id="efee2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efee2-129">CommonParameters</span></span>
<span data-ttu-id="efee2-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="efee2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efee2-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="efee2-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efee2-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="efee2-132">INPUTS</span></span>

## <span data-ttu-id="efee2-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="efee2-133">OUTPUTS</span></span>

## <span data-ttu-id="efee2-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="efee2-134">NOTES</span></span>

## <span data-ttu-id="efee2-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="efee2-135">RELATED LINKS</span></span>

[<span data-ttu-id="efee2-136">Set-AzureSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="efee2-136">Set-AzureSiteRecoveryVM</span></span>](./Set-AzureSiteRecoveryVM.md)


