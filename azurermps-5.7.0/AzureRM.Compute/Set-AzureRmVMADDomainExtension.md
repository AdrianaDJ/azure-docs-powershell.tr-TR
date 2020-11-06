---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 65BF37D3-4FCE-48A3-BC5D-01AA20FEB6CA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMADDomainExtension.md
ms.openlocfilehash: b0af0f205f26862c20dd50e6181d2c11cd050dd1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586780"
---
# <span data-ttu-id="dddba-101">Set-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="dddba-101">Set-AzureRmVMADDomainExtension</span></span>

## <span data-ttu-id="dddba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dddba-102">SYNOPSIS</span></span>
<span data-ttu-id="dddba-103">Bir sanal makineye AD alanı uzantısı ekler.</span><span class="sxs-lookup"><span data-stu-id="dddba-103">Adds an AD domain extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dddba-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dddba-104">SYNTAX</span></span>

```
Set-AzureRmVMADDomainExtension -DomainName <String> [-OUPath <String>] [-JoinOption <UInt32>]
 [-Credential <PSCredential>] [-Restart] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dddba-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="dddba-105">DESCRIPTION</span></span>
<span data-ttu-id="dddba-106">**Set-AzureRmVMADDomainExtension** cmdlet 'ı bir Azure Active DIRECTORY (ad) etki alanı sanal makine uzantısını bir sanal makineye ekler.</span><span class="sxs-lookup"><span data-stu-id="dddba-106">The **Set-AzureRmVMADDomainExtension** cmdlet adds an Azure Active Directory (AD) domain virtual machine extension to a virtual machine.</span></span>
<span data-ttu-id="dddba-107">Bu uzantı, sanal makinenizin bir etki alanına katılmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="dddba-107">This extension lets your virtual machine join a domain.</span></span>

## <span data-ttu-id="dddba-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dddba-108">EXAMPLES</span></span>

## <span data-ttu-id="dddba-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dddba-109">PARAMETERS</span></span>

### <span data-ttu-id="dddba-110">-Credential</span><span class="sxs-lookup"><span data-stu-id="dddba-110">-Credential</span></span>
<span data-ttu-id="dddba-111">Sanal makinenin bir **PSCredential** nesnesi olarak Kullanıcı adını ve parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dddba-111">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="dddba-112">Kimlik bilgilerini almak için Get-Credential cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="dddba-112">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="dddba-113">Daha fazla bilgi için yazın `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="dddba-113">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dddba-114">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="dddba-114">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="dddba-115">Bu cmdlet 'in, uzantının ara sürümünün otomatik yükseltmesini devre dışı bırakacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="dddba-115">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dddba-116">-EtkiAlanıAdı</span><span class="sxs-lookup"><span data-stu-id="dddba-116">-DomainName</span></span>
<span data-ttu-id="dddba-117">Etki alanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dddba-117">Specifies the name of the domain.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dddba-118">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="dddba-118">-ForceRerun</span></span>
<span data-ttu-id="dddba-119">Bu cmdlet 'in, uzantıyı kaldırıp yeniden yüklemeden sanal makinede aynı uzantı yapılandırmasını yeniden çalıştırmayı zortığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="dddba-119">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="dddba-120">Değer, geçerli değerden farklı olabilir.</span><span class="sxs-lookup"><span data-stu-id="dddba-120">The value can be any string different from the current value.</span></span>

<span data-ttu-id="dddba-121">ForceUpdateTag değiştirilirse, genel veya korumalı ayarlara yönelik güncelleştirmeler işleyici tarafından uygulanır.</span><span class="sxs-lookup"><span data-stu-id="dddba-121">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dddba-122">-JoinOption</span><span class="sxs-lookup"><span data-stu-id="dddba-122">-JoinOption</span></span>
<span data-ttu-id="dddba-123">Katılma seçeneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="dddba-123">Specifies the join option.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dddba-124">-Konum</span><span class="sxs-lookup"><span data-stu-id="dddba-124">-Location</span></span>
<span data-ttu-id="dddba-125">Sanal makinenin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="dddba-125">Specifies the location of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dddba-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="dddba-126">-Name</span></span>
<span data-ttu-id="dddba-127">Eklenecek etki alanı uzantısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dddba-127">Specifies the name of the domain extension to add.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dddba-128">-OUPath</span><span class="sxs-lookup"><span data-stu-id="dddba-128">-OUPath</span></span>
<span data-ttu-id="dddba-129">Etki alanı hesabı için bir kuruluş birimi (OU) belirtir.</span><span class="sxs-lookup"><span data-stu-id="dddba-129">Specifies an organizational unit (OU) for the domain account.</span></span>
<span data-ttu-id="dddba-130">KURULUŞ biriminin tam ayırt edici adını tırnak içine girin.</span><span class="sxs-lookup"><span data-stu-id="dddba-130">Enter the full distinguished name of the OU in quotation marks.</span></span>
<span data-ttu-id="dddba-131">Varsayılan değer, etki alanındaki makine nesnelerinin varsayılan OU 'dır.</span><span class="sxs-lookup"><span data-stu-id="dddba-131">The default value is the default OU for machine objects in the domain.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dddba-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dddba-132">-ResourceGroupName</span></span>
<span data-ttu-id="dddba-133">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dddba-133">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dddba-134">-Restart</span><span class="sxs-lookup"><span data-stu-id="dddba-134">-Restart</span></span>
<span data-ttu-id="dddba-135">Bu cmdlet 'in sanal makineyi yeniden başlattığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="dddba-135">Indicates that this cmdlet restarts the virtual machine.</span></span>
<span data-ttu-id="dddba-136">Değişikliğin etkili olması için genellikle yeniden başlatma gerekir.</span><span class="sxs-lookup"><span data-stu-id="dddba-136">A restart is often required to make the change effective.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dddba-137">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="dddba-137">-TypeHandlerVersion</span></span>
<span data-ttu-id="dddba-138">Etki alanı uzantısının sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="dddba-138">Specifies the version of the domain extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dddba-139">-VMName</span><span class="sxs-lookup"><span data-stu-id="dddba-139">-VMName</span></span>
<span data-ttu-id="dddba-140">Sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dddba-140">Specifies the name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dddba-141">-Onay</span><span class="sxs-lookup"><span data-stu-id="dddba-141">-Confirm</span></span>
<span data-ttu-id="dddba-142">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="dddba-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dddba-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dddba-143">-WhatIf</span></span>
<span data-ttu-id="dddba-144">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="dddba-144">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="dddba-145">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="dddba-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dddba-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dddba-146">CommonParameters</span></span>
<span data-ttu-id="dddba-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dddba-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dddba-148">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dddba-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dddba-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dddba-149">INPUTS</span></span>

### <span data-ttu-id="dddba-150">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="dddba-150">None</span></span>
<span data-ttu-id="dddba-151">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="dddba-151">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="dddba-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dddba-152">OUTPUTS</span></span>

## <span data-ttu-id="dddba-153">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dddba-153">NOTES</span></span>

## <span data-ttu-id="dddba-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dddba-154">RELATED LINKS</span></span>

[<span data-ttu-id="dddba-155">Get-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="dddba-155">Get-AzureRmVMADDomainExtension</span></span>](./Get-AzureRmVMADDomainExtension.md)
