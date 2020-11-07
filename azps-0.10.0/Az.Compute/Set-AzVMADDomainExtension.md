---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 65BF37D3-4FCE-48A3-BC5D-01AA20FEB6CA
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmaddomainextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMADDomainExtension.md
ms.openlocfilehash: 99dd311adf976e100282da92db6a3147880feefb
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936849"
---
# <span data-ttu-id="a77a1-101">Set-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="a77a1-101">Set-AzVMADDomainExtension</span></span>

## <span data-ttu-id="a77a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a77a1-102">SYNOPSIS</span></span>
<span data-ttu-id="a77a1-103">Bir sanal makineye AD alanı uzantısı ekler.</span><span class="sxs-lookup"><span data-stu-id="a77a1-103">Adds an AD domain extension to a virtual machine.</span></span>

## <span data-ttu-id="a77a1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a77a1-104">SYNTAX</span></span>

```
Set-AzVMADDomainExtension -DomainName <String> [-OUPath <String>] [-JoinOption <UInt32>]
 [-Credential <PSCredential>] [-Restart] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a77a1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a77a1-105">DESCRIPTION</span></span>
<span data-ttu-id="a77a1-106">**Set-AzVMADDomainExtension** cmdlet 'ı bir Azure Active DIRECTORY (ad) etki alanı sanal makine uzantısını bir sanal makineye ekler.</span><span class="sxs-lookup"><span data-stu-id="a77a1-106">The **Set-AzVMADDomainExtension** cmdlet adds an Azure Active Directory (AD) domain virtual machine extension to a virtual machine.</span></span>
<span data-ttu-id="a77a1-107">Bu uzantı, sanal makinenizin bir etki alanına katılmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="a77a1-107">This extension lets your virtual machine join a domain.</span></span>

## <span data-ttu-id="a77a1-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a77a1-108">EXAMPLES</span></span>

## <span data-ttu-id="a77a1-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a77a1-109">PARAMETERS</span></span>

### <span data-ttu-id="a77a1-110">-Credential</span><span class="sxs-lookup"><span data-stu-id="a77a1-110">-Credential</span></span>
<span data-ttu-id="a77a1-111">Sanal makinenin bir **PSCredential** nesnesi olarak Kullanıcı adını ve parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a77a1-111">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="a77a1-112">Kimlik bilgilerini almak için Get-Credential cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="a77a1-112">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="a77a1-113">Daha fazla bilgi için yazın `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="a77a1-113">For more information, type `Get-Help Get-Credential`.</span></span>

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

### <span data-ttu-id="a77a1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a77a1-114">-DefaultProfile</span></span>
<span data-ttu-id="a77a1-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a77a1-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a77a1-116">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="a77a1-116">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="a77a1-117">Bu cmdlet 'in, uzantının ara sürümünün otomatik yükseltmesini devre dışı bırakacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a77a1-117">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

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

### <span data-ttu-id="a77a1-118">-EtkiAlanıAdı</span><span class="sxs-lookup"><span data-stu-id="a77a1-118">-DomainName</span></span>
<span data-ttu-id="a77a1-119">Etki alanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a77a1-119">Specifies the name of the domain.</span></span>

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

### <span data-ttu-id="a77a1-120">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="a77a1-120">-ForceRerun</span></span>
<span data-ttu-id="a77a1-121">Bu cmdlet 'in, uzantıyı kaldırıp yeniden yüklemeden sanal makinede aynı uzantı yapılandırmasını yeniden çalıştırmayı zortığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a77a1-121">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="a77a1-122">Değer, geçerli değerden farklı olabilir.</span><span class="sxs-lookup"><span data-stu-id="a77a1-122">The value can be any string different from the current value.</span></span>

<span data-ttu-id="a77a1-123">ForceUpdateTag değiştirilirse, genel veya korumalı ayarlara yönelik güncelleştirmeler işleyici tarafından uygulanır.</span><span class="sxs-lookup"><span data-stu-id="a77a1-123">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="a77a1-124">-JoinOption</span><span class="sxs-lookup"><span data-stu-id="a77a1-124">-JoinOption</span></span>
<span data-ttu-id="a77a1-125">Katılma seçeneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a77a1-125">Specifies the join option.</span></span>

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

### <span data-ttu-id="a77a1-126">-Konum</span><span class="sxs-lookup"><span data-stu-id="a77a1-126">-Location</span></span>
<span data-ttu-id="a77a1-127">Sanal makinenin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="a77a1-127">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="a77a1-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="a77a1-128">-Name</span></span>
<span data-ttu-id="a77a1-129">Eklenecek etki alanı uzantısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a77a1-129">Specifies the name of the domain extension to add.</span></span>

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

### <span data-ttu-id="a77a1-130">-OUPath</span><span class="sxs-lookup"><span data-stu-id="a77a1-130">-OUPath</span></span>
<span data-ttu-id="a77a1-131">Etki alanı hesabı için bir kuruluş birimi (OU) belirtir.</span><span class="sxs-lookup"><span data-stu-id="a77a1-131">Specifies an organizational unit (OU) for the domain account.</span></span>
<span data-ttu-id="a77a1-132">KURULUŞ biriminin tam ayırt edici adını tırnak içine girin.</span><span class="sxs-lookup"><span data-stu-id="a77a1-132">Enter the full distinguished name of the OU in quotation marks.</span></span>
<span data-ttu-id="a77a1-133">Varsayılan değer, etki alanındaki makine nesnelerinin varsayılan OU 'dır.</span><span class="sxs-lookup"><span data-stu-id="a77a1-133">The default value is the default OU for machine objects in the domain.</span></span>

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

### <span data-ttu-id="a77a1-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a77a1-134">-ResourceGroupName</span></span>
<span data-ttu-id="a77a1-135">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a77a1-135">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="a77a1-136">-Restart</span><span class="sxs-lookup"><span data-stu-id="a77a1-136">-Restart</span></span>
<span data-ttu-id="a77a1-137">Bu cmdlet 'in sanal makineyi yeniden başlattığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a77a1-137">Indicates that this cmdlet restarts the virtual machine.</span></span>
<span data-ttu-id="a77a1-138">Değişikliğin etkili olması için genellikle yeniden başlatma gerekir.</span><span class="sxs-lookup"><span data-stu-id="a77a1-138">A restart is often required to make the change effective.</span></span>

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

### <span data-ttu-id="a77a1-139">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="a77a1-139">-TypeHandlerVersion</span></span>
<span data-ttu-id="a77a1-140">Etki alanı uzantısının sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="a77a1-140">Specifies the version of the domain extension.</span></span>

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

### <span data-ttu-id="a77a1-141">-VMName</span><span class="sxs-lookup"><span data-stu-id="a77a1-141">-VMName</span></span>
<span data-ttu-id="a77a1-142">Sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a77a1-142">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="a77a1-143">-Onay</span><span class="sxs-lookup"><span data-stu-id="a77a1-143">-Confirm</span></span>
<span data-ttu-id="a77a1-144">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a77a1-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a77a1-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a77a1-145">-WhatIf</span></span>
<span data-ttu-id="a77a1-146">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a77a1-146">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="a77a1-147">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a77a1-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a77a1-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a77a1-148">CommonParameters</span></span>
<span data-ttu-id="a77a1-149">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a77a1-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a77a1-150">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a77a1-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a77a1-151">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a77a1-151">INPUTS</span></span>

### <span data-ttu-id="a77a1-152">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="a77a1-152">None</span></span>
<span data-ttu-id="a77a1-153">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="a77a1-153">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a77a1-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a77a1-154">OUTPUTS</span></span>

### <span data-ttu-id="a77a1-155">Microsoft. Azure. Commands. COMPUTE. modeller. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="a77a1-155">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="a77a1-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a77a1-156">NOTES</span></span>

## <span data-ttu-id="a77a1-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a77a1-157">RELATED LINKS</span></span>

[<span data-ttu-id="a77a1-158">Get-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="a77a1-158">Get-AzVMADDomainExtension</span></span>](./Get-AzVMADDomainExtension.md)
