---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 65BF37D3-4FCE-48A3-BC5D-01AA20FEB6CA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmaddomainextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMADDomainExtension.md
ms.openlocfilehash: e0d36e8ddc239d1d075b79e0c91df645d671c6a3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594430"
---
# <span data-ttu-id="7cb0b-101">Set-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="7cb0b-101">Set-AzureRmVMADDomainExtension</span></span>

## <span data-ttu-id="7cb0b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7cb0b-102">SYNOPSIS</span></span>
<span data-ttu-id="7cb0b-103">Bir sanal makineye AD alanı uzantısı ekler.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-103">Adds an AD domain extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7cb0b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7cb0b-104">SYNTAX</span></span>

```
Set-AzureRmVMADDomainExtension -DomainName <String> [-OUPath <String>] [-JoinOption <UInt32>]
 [-Credential <PSCredential>] [-Restart] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7cb0b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7cb0b-105">DESCRIPTION</span></span>
<span data-ttu-id="7cb0b-106">**Set-AzureRmVMADDomainExtension** cmdlet 'ı bir Azure Active DIRECTORY (ad) etki alanı sanal makine uzantısını bir sanal makineye ekler.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-106">The **Set-AzureRmVMADDomainExtension** cmdlet adds an Azure Active Directory (AD) domain virtual machine extension to a virtual machine.</span></span>
<span data-ttu-id="7cb0b-107">Bu uzantı, sanal makinenizin bir etki alanına katılmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-107">This extension lets your virtual machine join a domain.</span></span>

## <span data-ttu-id="7cb0b-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7cb0b-108">EXAMPLES</span></span>

## <span data-ttu-id="7cb0b-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7cb0b-109">PARAMETERS</span></span>

### <span data-ttu-id="7cb0b-110">-Credential</span><span class="sxs-lookup"><span data-stu-id="7cb0b-110">-Credential</span></span>
<span data-ttu-id="7cb0b-111">Sanal makinenin bir **PSCredential** nesnesi olarak Kullanıcı adını ve parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-111">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="7cb0b-112">Kimlik bilgilerini almak için Get-Credential cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-112">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="7cb0b-113">Daha fazla bilgi için yazın `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="7cb0b-113">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cb0b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cb0b-114">-DefaultProfile</span></span>
<span data-ttu-id="7cb0b-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cb0b-116">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="7cb0b-116">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="7cb0b-117">Bu cmdlet 'in, uzantının ara sürümünün otomatik yükseltmesini devre dışı bırakacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-117">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cb0b-118">-EtkiAlanıAdı</span><span class="sxs-lookup"><span data-stu-id="7cb0b-118">-DomainName</span></span>
<span data-ttu-id="7cb0b-119">Etki alanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-119">Specifies the name of the domain.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cb0b-120">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="7cb0b-120">-ForceRerun</span></span>
<span data-ttu-id="7cb0b-121">Bu cmdlet 'in, uzantıyı kaldırıp yeniden yüklemeden sanal makinede aynı uzantı yapılandırmasını yeniden çalıştırmayı zortığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-121">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="7cb0b-122">Değer, geçerli değerden farklı olabilir.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-122">The value can be any string different from the current value.</span></span>
<span data-ttu-id="7cb0b-123">ForceUpdateTag değiştirilirse, genel veya korumalı ayarlara yönelik güncelleştirmeler işleyici tarafından uygulanır.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-123">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cb0b-124">-JoinOption</span><span class="sxs-lookup"><span data-stu-id="7cb0b-124">-JoinOption</span></span>
<span data-ttu-id="7cb0b-125">Katılma seçeneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-125">Specifies the join option.</span></span> <span data-ttu-id="7cb0b-126">Birleştirme seçenekleri için bkz: [FJoinOptions](https://docs.microsoft.com/en-us/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain)</span><span class="sxs-lookup"><span data-stu-id="7cb0b-126">For join options see [fJoinOptions](https://docs.microsoft.com/en-us/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain)</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cb0b-127">-Konum</span><span class="sxs-lookup"><span data-stu-id="7cb0b-127">-Location</span></span>
<span data-ttu-id="7cb0b-128">Sanal makinenin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-128">Specifies the location of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cb0b-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="7cb0b-129">-Name</span></span>
<span data-ttu-id="7cb0b-130">Eklenecek etki alanı uzantısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-130">Specifies the name of the domain extension to add.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cb0b-131">-OUPath</span><span class="sxs-lookup"><span data-stu-id="7cb0b-131">-OUPath</span></span>
<span data-ttu-id="7cb0b-132">Etki alanı hesabı için bir kuruluş birimi (OU) belirtir.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-132">Specifies an organizational unit (OU) for the domain account.</span></span>
<span data-ttu-id="7cb0b-133">KURULUŞ biriminin tam ayırt edici adını tırnak içine girin.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-133">Enter the full distinguished name of the OU in quotation marks.</span></span>
<span data-ttu-id="7cb0b-134">Varsayılan değer, etki alanındaki makine nesnelerinin varsayılan OU 'dır.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-134">The default value is the default OU for machine objects in the domain.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cb0b-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7cb0b-135">-ResourceGroupName</span></span>
<span data-ttu-id="7cb0b-136">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-136">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cb0b-137">-Restart</span><span class="sxs-lookup"><span data-stu-id="7cb0b-137">-Restart</span></span>
<span data-ttu-id="7cb0b-138">Bu cmdlet 'in sanal makineyi yeniden başlattığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-138">Indicates that this cmdlet restarts the virtual machine.</span></span>
<span data-ttu-id="7cb0b-139">Değişikliğin etkili olması için genellikle yeniden başlatma gerekir.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-139">A restart is often required to make the change effective.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cb0b-140">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="7cb0b-140">-TypeHandlerVersion</span></span>
<span data-ttu-id="7cb0b-141">Etki alanı uzantısının sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-141">Specifies the version of the domain extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cb0b-142">-VMName</span><span class="sxs-lookup"><span data-stu-id="7cb0b-142">-VMName</span></span>
<span data-ttu-id="7cb0b-143">Sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-143">Specifies the name of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cb0b-144">-Onay</span><span class="sxs-lookup"><span data-stu-id="7cb0b-144">-Confirm</span></span>
<span data-ttu-id="7cb0b-145">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cb0b-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7cb0b-146">-WhatIf</span></span>
<span data-ttu-id="7cb0b-147">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7cb0b-148">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-148">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cb0b-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cb0b-149">CommonParameters</span></span>
<span data-ttu-id="7cb0b-150">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cb0b-151">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7cb0b-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cb0b-152">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7cb0b-152">INPUTS</span></span>

### <span data-ttu-id="7cb0b-153">System. String</span><span class="sxs-lookup"><span data-stu-id="7cb0b-153">System.String</span></span>

### <span data-ttu-id="7cb0b-154">System. Nullable ' 1 [[System. UInt32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="7cb0b-154">System.Nullable\`1[[System.UInt32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="7cb0b-155">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="7cb0b-155">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="7cb0b-156">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7cb0b-156">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7cb0b-157">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7cb0b-157">OUTPUTS</span></span>

### <span data-ttu-id="7cb0b-158">Microsoft. Azure. Commands. COMPUTE. modeller. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="7cb0b-158">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="7cb0b-159">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7cb0b-159">NOTES</span></span>

## <span data-ttu-id="7cb0b-160">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7cb0b-160">RELATED LINKS</span></span>

[<span data-ttu-id="7cb0b-161">Get-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="7cb0b-161">Get-AzureRmVMADDomainExtension</span></span>](./Get-AzureRmVMADDomainExtension.md)
