---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 65BF37D3-4FCE-48A3-BC5D-01AA20FEB6CA
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmaddomainextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMADDomainExtension.md
ms.openlocfilehash: fed235e3c628ab245ae74299cf395e4501b141f7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752711"
---
# <span data-ttu-id="46d69-101">Set-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="46d69-101">Set-AzVMADDomainExtension</span></span>

## <span data-ttu-id="46d69-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46d69-102">SYNOPSIS</span></span>
<span data-ttu-id="46d69-103">Bir sanal makineye AD alanı uzantısı ekler.</span><span class="sxs-lookup"><span data-stu-id="46d69-103">Adds an AD domain extension to a virtual machine.</span></span>

## <span data-ttu-id="46d69-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="46d69-104">SYNTAX</span></span>

```
Set-AzVMADDomainExtension -DomainName <String> [-OUPath <String>] [-JoinOption <UInt32>]
 [-Credential <PSCredential>] [-Restart] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46d69-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="46d69-105">DESCRIPTION</span></span>
<span data-ttu-id="46d69-106">**Set-AzVMADDomainExtension** cmdlet 'ı bir Azure Active DIRECTORY (ad) etki alanı sanal makine uzantısını bir sanal makineye ekler.</span><span class="sxs-lookup"><span data-stu-id="46d69-106">The **Set-AzVMADDomainExtension** cmdlet adds an Azure Active Directory (AD) domain virtual machine extension to a virtual machine.</span></span>
<span data-ttu-id="46d69-107">Bu uzantı, sanal makinenizin bir etki alanına katılmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="46d69-107">This extension lets your virtual machine join a domain.</span></span>

## <span data-ttu-id="46d69-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="46d69-108">EXAMPLES</span></span>

## <span data-ttu-id="46d69-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="46d69-109">PARAMETERS</span></span>

### <span data-ttu-id="46d69-110">-Credential</span><span class="sxs-lookup"><span data-stu-id="46d69-110">-Credential</span></span>
<span data-ttu-id="46d69-111">Sanal makinenin bir **PSCredential** nesnesi olarak Kullanıcı adını ve parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="46d69-111">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="46d69-112">Kimlik bilgilerini almak için Get-Credential cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="46d69-112">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="46d69-113">Daha fazla bilgi için yazın `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="46d69-113">For more information, type `Get-Help Get-Credential`.</span></span>

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

### <span data-ttu-id="46d69-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46d69-114">-DefaultProfile</span></span>
<span data-ttu-id="46d69-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="46d69-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46d69-116">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="46d69-116">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="46d69-117">Bu cmdlet 'in, uzantının ara sürümünün otomatik yükseltmesini devre dışı bırakacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="46d69-117">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

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

### <span data-ttu-id="46d69-118">-EtkiAlanıAdı</span><span class="sxs-lookup"><span data-stu-id="46d69-118">-DomainName</span></span>
<span data-ttu-id="46d69-119">Etki alanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="46d69-119">Specifies the name of the domain.</span></span>

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

### <span data-ttu-id="46d69-120">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="46d69-120">-ForceRerun</span></span>
<span data-ttu-id="46d69-121">Bu cmdlet 'in, uzantıyı kaldırıp yeniden yüklemeden sanal makinede aynı uzantı yapılandırmasını yeniden çalıştırmayı zortığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="46d69-121">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="46d69-122">Değer, geçerli değerden farklı olabilir.</span><span class="sxs-lookup"><span data-stu-id="46d69-122">The value can be any string different from the current value.</span></span>
<span data-ttu-id="46d69-123">ForceUpdateTag değiştirilirse, genel veya korumalı ayarlara yönelik güncelleştirmeler işleyici tarafından uygulanır.</span><span class="sxs-lookup"><span data-stu-id="46d69-123">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="46d69-124">-JoinOption</span><span class="sxs-lookup"><span data-stu-id="46d69-124">-JoinOption</span></span>
<span data-ttu-id="46d69-125">Katılma seçeneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="46d69-125">Specifies the join option.</span></span> <span data-ttu-id="46d69-126">Birleştirme seçenekleri için bkz: [FJoinOptions](https://docs.microsoft.com/en-us/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain)</span><span class="sxs-lookup"><span data-stu-id="46d69-126">For join options see [fJoinOptions](https://docs.microsoft.com/en-us/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain)</span></span>

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

### <span data-ttu-id="46d69-127">-Konum</span><span class="sxs-lookup"><span data-stu-id="46d69-127">-Location</span></span>
<span data-ttu-id="46d69-128">Sanal makinenin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="46d69-128">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="46d69-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="46d69-129">-Name</span></span>
<span data-ttu-id="46d69-130">Eklenecek etki alanı uzantısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="46d69-130">Specifies the name of the domain extension to add.</span></span>

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

### <span data-ttu-id="46d69-131">-NoWait</span><span class="sxs-lookup"><span data-stu-id="46d69-131">-NoWait</span></span>
<span data-ttu-id="46d69-132">İşlemi başlatır ve işlem tamamlanmadan hemen döner.</span><span class="sxs-lookup"><span data-stu-id="46d69-132">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="46d69-133">İşlemin başarıyla tamamlanıp tamamlanmadığını belirlemek için başka bir mekanizma kullanın.</span><span class="sxs-lookup"><span data-stu-id="46d69-133">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46d69-134">-OUPath</span><span class="sxs-lookup"><span data-stu-id="46d69-134">-OUPath</span></span>
<span data-ttu-id="46d69-135">Etki alanı hesabı için bir kuruluş birimi (OU) belirtir.</span><span class="sxs-lookup"><span data-stu-id="46d69-135">Specifies an organizational unit (OU) for the domain account.</span></span>
<span data-ttu-id="46d69-136">KURULUŞ biriminin tam ayırt edici adını tırnak içine girin.</span><span class="sxs-lookup"><span data-stu-id="46d69-136">Enter the full distinguished name of the OU in quotation marks.</span></span>
<span data-ttu-id="46d69-137">Varsayılan değer, etki alanındaki makine nesnelerinin varsayılan OU 'dır.</span><span class="sxs-lookup"><span data-stu-id="46d69-137">The default value is the default OU for machine objects in the domain.</span></span>

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

### <span data-ttu-id="46d69-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46d69-138">-ResourceGroupName</span></span>
<span data-ttu-id="46d69-139">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="46d69-139">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="46d69-140">-Restart</span><span class="sxs-lookup"><span data-stu-id="46d69-140">-Restart</span></span>
<span data-ttu-id="46d69-141">Bu cmdlet 'in sanal makineyi yeniden başlattığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="46d69-141">Indicates that this cmdlet restarts the virtual machine.</span></span>
<span data-ttu-id="46d69-142">Değişikliğin etkili olması için genellikle yeniden başlatma gerekir.</span><span class="sxs-lookup"><span data-stu-id="46d69-142">A restart is often required to make the change effective.</span></span>

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

### <span data-ttu-id="46d69-143">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="46d69-143">-TypeHandlerVersion</span></span>
<span data-ttu-id="46d69-144">Etki alanı uzantısının sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="46d69-144">Specifies the version of the domain extension.</span></span>

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

### <span data-ttu-id="46d69-145">-VMName</span><span class="sxs-lookup"><span data-stu-id="46d69-145">-VMName</span></span>
<span data-ttu-id="46d69-146">Sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="46d69-146">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="46d69-147">-Onay</span><span class="sxs-lookup"><span data-stu-id="46d69-147">-Confirm</span></span>
<span data-ttu-id="46d69-148">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="46d69-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46d69-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46d69-149">-WhatIf</span></span>
<span data-ttu-id="46d69-150">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="46d69-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46d69-151">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="46d69-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46d69-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46d69-152">CommonParameters</span></span>
<span data-ttu-id="46d69-153">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="46d69-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46d69-154">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="46d69-154">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46d69-155">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="46d69-155">INPUTS</span></span>

### <span data-ttu-id="46d69-156">System. String</span><span class="sxs-lookup"><span data-stu-id="46d69-156">System.String</span></span>

### <span data-ttu-id="46d69-157">System. Nullable ' 1 [[System. UInt32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="46d69-157">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="46d69-158">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="46d69-158">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="46d69-159">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="46d69-159">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="46d69-160">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="46d69-160">OUTPUTS</span></span>

### <span data-ttu-id="46d69-161">Microsoft. Azure. Commands. COMPUTE. modeller. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="46d69-161">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="46d69-162">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="46d69-162">NOTES</span></span>

## <span data-ttu-id="46d69-163">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="46d69-163">RELATED LINKS</span></span>

[<span data-ttu-id="46d69-164">Get-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="46d69-164">Get-AzVMADDomainExtension</span></span>](./Get-AzVMADDomainExtension.md)