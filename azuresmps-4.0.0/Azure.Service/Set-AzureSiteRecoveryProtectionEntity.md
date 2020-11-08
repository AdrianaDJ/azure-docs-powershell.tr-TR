---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 1415BBA3-3F55-46A9-B20B-DFA72342BDF4
online version: ''
schema: 2.0.0
ms.openlocfilehash: ec7883b996e5da367884fd7d051a5299c6d62a9e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106423"
---
# <span data-ttu-id="ac0f8-101">Set-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="ac0f8-101">Set-AzureSiteRecoveryProtectionEntity</span></span>

## <span data-ttu-id="ac0f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac0f8-102">SYNOPSIS</span></span>
<span data-ttu-id="ac0f8-103">Site kurtarma koruma varlığının durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="ac0f8-103">Sets the state for a Site Recovery protection entity.</span></span>

## <span data-ttu-id="ac0f8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ac0f8-104">SYNTAX</span></span>

### <span data-ttu-id="ac0f8-105">Btypeınfo (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ac0f8-105">ByPEObject (Default)</span></span>
```
Set-AzureSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity>
 [-ProtectionProfile <ASRProtectionProfile>] -Protection <String> [-OSDiskName <String>] [-OS <String>]
 [-WaitForCompletion] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac0f8-106">Kimlikler</span><span class="sxs-lookup"><span data-stu-id="ac0f8-106">ByIDs</span></span>
```
Set-AzureSiteRecoveryProtectionEntity -Id <String> -ProtectionContainerId <String>
 [-ProtectionProfile <ASRProtectionProfile>] -Protection <String> [-OSDiskName <String>] [-OS <String>]
 [-WaitForCompletion] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac0f8-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="ac0f8-107">DESCRIPTION</span></span>
<span data-ttu-id="ac0f8-108">**Set-AzureSiteRecoveryProtectionEntity** cmdlet 'ı bir Azure Site Recovery koruma varlığında korumayı devre dışı bırakır veya devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="ac0f8-108">The **Set-AzureSiteRecoveryProtectionEntity** cmdlet enables or disables protection on an Azure Site Recovery protection entity.</span></span>

## <span data-ttu-id="ac0f8-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ac0f8-109">EXAMPLES</span></span>

### <span data-ttu-id="ac0f8-110">Örnek 1: kapsayıcıdaki nesneler için korumayı etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="ac0f8-110">Example 1: Enable protection for objects in a container</span></span>
```
PS C:\> $ProtectionContainer = Get-AzureSiteRecoveryProtectionContainer -Name "Cloud17"
PS C:\> $ProtectionEntity = Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $ProtectionContainer -Name "VM01"
PS C:\> Set-AzureSiteRecoveryProtectionEntity -ProtectionEntity $ ProtectionEntity -Protection Enable -ProtectionProfile $ProtectionContainer.AvailableProtectionProfiles[0] -OS Windows
```

<span data-ttu-id="ac0f8-111">İlk komut **Get-AzureSiteRecoveryProtectionContainer** cmdlet 'ini kullanarak geçerli Azure Site Kasası kapsayıcılarını alır ve ardından $ProtectionContainer değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="ac0f8-111">The first command gets containers for the current Azure Site vault by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores it in the $ProtectionContainer variable.</span></span>

<span data-ttu-id="ac0f8-112">İkinci komut, **Get-AzureSiteRecoveryProtectionEntity** cmdlet 'ini kullanarak $ProtectionContainer depolanan kapsayıcıya ait korumalı sanal makineleri alır.</span><span class="sxs-lookup"><span data-stu-id="ac0f8-112">The second command gets the protected virtual machines that belong to the container stored in $ProtectionContainer by using the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>
<span data-ttu-id="ac0f8-113">Komut sonuçları $ProtectionEntity değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="ac0f8-113">The command stores the results in the $ProtectionEntity variable.</span></span>

<span data-ttu-id="ac0f8-114">Son komutu, $ProtectionEntity depolanan varlıklar için koruma etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="ac0f8-114">The final command enables protection for the entities stored in $ProtectionEntity.</span></span>

## <span data-ttu-id="ac0f8-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ac0f8-115">PARAMETERS</span></span>

### <span data-ttu-id="ac0f8-116">-Force</span><span class="sxs-lookup"><span data-stu-id="ac0f8-116">-Force</span></span>
<span data-ttu-id="ac0f8-117">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="ac0f8-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ac0f8-118">-ID</span><span class="sxs-lookup"><span data-stu-id="ac0f8-118">-Id</span></span>
<span data-ttu-id="ac0f8-119">Korumayı etkinleştirmek veya devre dışı bırakmak için korumalı sanal makinenin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="ac0f8-119">Specifies the ID of a protected virtual machine for which to enable or disable protection.</span></span>

```yaml
Type: String
Parameter Sets: ByIDs
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac0f8-120">-İşletim sistemi</span><span class="sxs-lookup"><span data-stu-id="ac0f8-120">-OS</span></span>
<span data-ttu-id="ac0f8-121">İşletim sistemi türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="ac0f8-121">Specifies the operating system type.</span></span>
<span data-ttu-id="ac0f8-122">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="ac0f8-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ac0f8-123">WINDOWS</span><span class="sxs-lookup"><span data-stu-id="ac0f8-123">Windows</span></span>
- <span data-ttu-id="ac0f8-124">UX</span><span class="sxs-lookup"><span data-stu-id="ac0f8-124">Linux</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac0f8-125">-OSDiskName</span><span class="sxs-lookup"><span data-stu-id="ac0f8-125">-OSDiskName</span></span>
<span data-ttu-id="ac0f8-126">İşletim sistemini içeren diskin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ac0f8-126">Specifies the name of the disk that contains the operating system.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac0f8-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="ac0f8-127">-Profile</span></span>
<span data-ttu-id="ac0f8-128">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ac0f8-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ac0f8-129">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="ac0f8-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ac0f8-130">-Koruma</span><span class="sxs-lookup"><span data-stu-id="ac0f8-130">-Protection</span></span>
<span data-ttu-id="ac0f8-131">Korumanın etkinleştirilip etkinleştirilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ac0f8-131">Specifies whether protection should be enabled or disabled.</span></span>
<span data-ttu-id="ac0f8-132">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="ac0f8-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ac0f8-133">Etkinleştiremez</span><span class="sxs-lookup"><span data-stu-id="ac0f8-133">Enable</span></span>
- <span data-ttu-id="ac0f8-134">Bırakılacağı</span><span class="sxs-lookup"><span data-stu-id="ac0f8-134">Disable</span></span>

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

### <span data-ttu-id="ac0f8-135">-Protectioncontainerıd</span><span class="sxs-lookup"><span data-stu-id="ac0f8-135">-ProtectionContainerId</span></span>
<span data-ttu-id="ac0f8-136">Korumalı bir kapsayıcının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="ac0f8-136">Specifies the ID of a protected container.</span></span>
<span data-ttu-id="ac0f8-137">Bu cmdlet, bu parametrenin belirttiği kapsayıcıya ait bir sanal makine için korumayı etkinleştirilir veya devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="ac0f8-137">This cmdlet enables or disables protection for a virtual machine that belongs to the container that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByIDs
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac0f8-138">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="ac0f8-138">-ProtectionEntity</span></span>
<span data-ttu-id="ac0f8-139">Koruma varlık nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ac0f8-139">Specifies the protection entity object.</span></span>

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

### <span data-ttu-id="ac0f8-140">-ProtectionProfile</span><span class="sxs-lookup"><span data-stu-id="ac0f8-140">-ProtectionProfile</span></span>
<span data-ttu-id="ac0f8-141">Korumayı etkinleştirmek için bir koruma profili belirtir.</span><span class="sxs-lookup"><span data-stu-id="ac0f8-141">Specifies a protection profile to enable protection.</span></span>
<span data-ttu-id="ac0f8-142">İlişkili koruma kapsayıcısındaki kullanılabilir koruma profillerinden biri olan bir **Asrprotectionprofile** nesnesi belirtin.</span><span class="sxs-lookup"><span data-stu-id="ac0f8-142">Specify an **ASRProtectionProfile** object that is one of the available protection profiles in the associated protection container.</span></span>

```yaml
Type: ASRProtectionProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac0f8-143">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="ac0f8-143">-WaitForCompletion</span></span>
<span data-ttu-id="ac0f8-144">Cmdlet 'in denetimi Windows PowerShell konsoluna göndermeden önce işlemin tamamlanmasını beklediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="ac0f8-144">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="ac0f8-145">-Onay</span><span class="sxs-lookup"><span data-stu-id="ac0f8-145">-Confirm</span></span>
<span data-ttu-id="ac0f8-146">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ac0f8-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac0f8-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac0f8-147">-WhatIf</span></span>
<span data-ttu-id="ac0f8-148">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ac0f8-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac0f8-149">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ac0f8-149">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac0f8-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac0f8-150">CommonParameters</span></span>
<span data-ttu-id="ac0f8-151">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ac0f8-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac0f8-152">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac0f8-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac0f8-153">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ac0f8-153">INPUTS</span></span>

## <span data-ttu-id="ac0f8-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ac0f8-154">OUTPUTS</span></span>

## <span data-ttu-id="ac0f8-155">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ac0f8-155">NOTES</span></span>

## <span data-ttu-id="ac0f8-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ac0f8-156">RELATED LINKS</span></span>

[<span data-ttu-id="ac0f8-157">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="ac0f8-157">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="ac0f8-158">Get-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="ac0f8-158">Get-AzureSiteRecoveryProtectionEntity</span></span>](./Get-AzureSiteRecoveryProtectionEntity.md)

[<span data-ttu-id="ac0f8-159">Güncelleştirme-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="ac0f8-159">Update-AzureSiteRecoveryProtectionEntity</span></span>](./Update-AzureSiteRecoveryProtectionEntity.md)


