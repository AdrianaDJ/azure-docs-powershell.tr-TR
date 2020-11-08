---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 870EE77E-57D9-4B52-9F80-CB24D642E6E7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4f94d95b40fb89f0c1df89ad0c8a9b78eb283184
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106400"
---
# <span data-ttu-id="5bc08-101">Update-AzureSiteRecoveryProtectionDirection</span><span class="sxs-lookup"><span data-stu-id="5bc08-101">Update-AzureSiteRecoveryProtectionDirection</span></span>

## <span data-ttu-id="5bc08-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5bc08-102">SYNOPSIS</span></span>
<span data-ttu-id="5bc08-103">Site kurtarma nesnesinin korunması için kaynak ve hedef sunucuyu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="5bc08-103">Updates the source and target server for the protection of a Site Recovery object.</span></span>

## <span data-ttu-id="5bc08-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5bc08-104">SYNTAX</span></span>

### <span data-ttu-id="5bc08-105">ByRPObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5bc08-105">ByRPObject (Default)</span></span>
```
Update-AzureSiteRecoveryProtectionDirection -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="5bc08-106">Byrpıd</span><span class="sxs-lookup"><span data-stu-id="5bc08-106">ByRPId</span></span>
```
Update-AzureSiteRecoveryProtectionDirection -RPId <String> -Direction <String> [-WaitForCompletion]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="5bc08-107">Kod</span><span class="sxs-lookup"><span data-stu-id="5bc08-107">ByPEId</span></span>
```
Update-AzureSiteRecoveryProtectionDirection -ProtectionEntityId <String> -ProtectionContainerId <String>
 -Direction <String> [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="5bc08-108">Btypeınfo</span><span class="sxs-lookup"><span data-stu-id="5bc08-108">ByPEObject</span></span>
```
Update-AzureSiteRecoveryProtectionDirection -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="5bc08-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="5bc08-109">DESCRIPTION</span></span>
<span data-ttu-id="5bc08-110">**Update-AzureSiteRecoveryProtectionDirection** cmdlet 'i, bir Azure Site Recovery nesnesinin yürütme işlemi tamamlandıktan sonra korunması için kaynak ve hedef sunucuyu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="5bc08-110">The **Update-AzureSiteRecoveryProtectionDirection** cmdlet updates the source and target server for the protection of an Azure Site Recovery object after a commit failover operation finishes.</span></span>

## <span data-ttu-id="5bc08-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5bc08-111">EXAMPLES</span></span>

### <span data-ttu-id="5bc08-112">Örnek 1: kapsayıcıda korumalı nesnenin yönünü değiştirme</span><span class="sxs-lookup"><span data-stu-id="5bc08-112">Example 1: Modify the direction for a protected object in a container</span></span>
```
PS C:\> $Container = Get-AzureSiteRecoveryProtectionContainer 
PS C:\> $Protected = Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $Container  
PS C:\> Update-AzureSiteRecoveryProtectionDirection -Direction RecoveryToPrimary -ProtectionEntity $Protected 
ID               : c38eecdc-731c-405b-a61c-08db99aae2fe
ClientRequestId  : 32ace403-0916-4967-83a1-529176bd6e88-2014-49-06 15:49:24Z-P
State            : NotStarted
StateDescription : NotStarted
StartTime        : 
EndTime          : 
AllowedActions   : {}
Name             : 
Tasks            : {}
Errors           : {}
```

<span data-ttu-id="5bc08-113">İlk komut, **Get-AzureSiteRecoveryProtectionContainer** cmdlet 'ini kullanarak geçerli Azure Site Recovery kasasındaki korumalı kapsayıcıları alır ve ardından $Container değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="5bc08-113">The first command gets the protected containers in the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores it in the $Container variable.</span></span>

<span data-ttu-id="5bc08-114">İkinci komut, **Get-AzureSiteRecoveryProtectionEntity** cmdlet 'ini kullanarak $Container depolanan kapsayıcıya ait sanal makineleri alır.</span><span class="sxs-lookup"><span data-stu-id="5bc08-114">The second command gets the virtual machines that belong to the container stored in $Container by using the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>
<span data-ttu-id="5bc08-115">Komut sonuçları $Protected değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="5bc08-115">The command stores the results in the $Protected variable.</span></span>

<span data-ttu-id="5bc08-116">Son komutu, $Protected depolanan nesneler için kurtarılan yönü ayarlar.</span><span class="sxs-lookup"><span data-stu-id="5bc08-116">The final command sets the direction to RecoverToPrimary for the objects stored in $Protected.</span></span>

## <span data-ttu-id="5bc08-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5bc08-117">PARAMETERS</span></span>

### <span data-ttu-id="5bc08-118">-Yön</span><span class="sxs-lookup"><span data-stu-id="5bc08-118">-Direction</span></span>
<span data-ttu-id="5bc08-119">Kaydetmenin yönünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="5bc08-119">Specifies the direction of the commit.</span></span>
<span data-ttu-id="5bc08-120">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="5bc08-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5bc08-121">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="5bc08-121">PrimaryToRecovery</span></span>
- <span data-ttu-id="5bc08-122">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="5bc08-122">RecoveryToPrimary</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bc08-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="5bc08-123">-Profile</span></span>
<span data-ttu-id="5bc08-124">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5bc08-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5bc08-125">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="5bc08-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5bc08-126">-Protectioncontainerıd</span><span class="sxs-lookup"><span data-stu-id="5bc08-126">-ProtectionContainerId</span></span>
<span data-ttu-id="5bc08-127">Korumalı bir kapsayıcının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="5bc08-127">Specifies the ID of a protected container.</span></span>
<span data-ttu-id="5bc08-128">Bu cmdlet, bu parametrenin belirttiği kapsayıcıya ait korumalı bir sanal makinenin yönünü değiştirir.</span><span class="sxs-lookup"><span data-stu-id="5bc08-128">This cmdlet modifies the direction for a protected virtual machine that belongs to the container that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByPEId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bc08-129">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="5bc08-129">-ProtectionEntity</span></span>
<span data-ttu-id="5bc08-130">Koruma varlık nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5bc08-130">Specifies the protection entity object.</span></span>

```yaml
Type: ASRProtectionEntity
Parameter Sets: ByPEObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5bc08-131">-Protectionentityıd</span><span class="sxs-lookup"><span data-stu-id="5bc08-131">-ProtectionEntityId</span></span>
<span data-ttu-id="5bc08-132">Korumalı bir sanal makinenin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="5bc08-132">Specifies the ID of a protected virtual machine.</span></span>
<span data-ttu-id="5bc08-133">Bu cmdlet, bu parametrenin belirttiği korumalı sanal makinenin yönünü değiştirir.</span><span class="sxs-lookup"><span data-stu-id="5bc08-133">This cmdlet modifies the direction for the protected virtual machine that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByPEId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bc08-134">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="5bc08-134">-RecoveryPlan</span></span>
<span data-ttu-id="5bc08-135">Kurtarma planı nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5bc08-135">Specifies a recovery plan object.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5bc08-136">-RPID</span><span class="sxs-lookup"><span data-stu-id="5bc08-136">-RPId</span></span>
<span data-ttu-id="5bc08-137">Kurtarma planının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="5bc08-137">Specifies the ID of a recovery plan.</span></span>
<span data-ttu-id="5bc08-138">Bu cmdlet, bu parametrenin belirttiği kurtarma planının yönünü değiştirir.</span><span class="sxs-lookup"><span data-stu-id="5bc08-138">This cmdlet modifies the direction for the recovery plan that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByRPId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bc08-139">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="5bc08-139">-WaitForCompletion</span></span>
<span data-ttu-id="5bc08-140">Cmdlet 'in denetimi Windows PowerShell konsoluna göndermeden önce işlemin tamamlanmasını beklediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="5bc08-140">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bc08-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bc08-141">CommonParameters</span></span>
<span data-ttu-id="5bc08-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5bc08-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bc08-143">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5bc08-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bc08-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5bc08-144">INPUTS</span></span>

## <span data-ttu-id="5bc08-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5bc08-145">OUTPUTS</span></span>

## <span data-ttu-id="5bc08-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5bc08-146">NOTES</span></span>

## <span data-ttu-id="5bc08-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5bc08-147">RELATED LINKS</span></span>

[<span data-ttu-id="5bc08-148">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="5bc08-148">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="5bc08-149">Get-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="5bc08-149">Get-AzureSiteRecoveryProtectionEntity</span></span>](./Get-AzureSiteRecoveryProtectionEntity.md)


