---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 65BF37D3-4FCE-48A3-BC5D-01AA20FEB6CA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmaddomainextension
schema: 2.0.0
ms.openlocfilehash: 140f1ccdedd6f3b3402601a8a844092bf3d7ab0e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939945"
---
# <span data-ttu-id="eca44-101">Set-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="eca44-101">Set-AzureRmVMADDomainExtension</span></span>

## <span data-ttu-id="eca44-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eca44-102">SYNOPSIS</span></span>
<span data-ttu-id="eca44-103">Bir sanal makineye AD alanı uzantısı ekler.</span><span class="sxs-lookup"><span data-stu-id="eca44-103">Adds an AD domain extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eca44-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="eca44-104">SYNTAX</span></span>

```
Set-AzureRmVMADDomainExtension -DomainName <String> [-OUPath <String>] [-JoinOption <UInt32>]
 [-Credential <PSCredential>] [-Restart] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eca44-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="eca44-105">DESCRIPTION</span></span>
<span data-ttu-id="eca44-106">**Set-AzureRmVMADDomainExtension** cmdlet 'ı bir Azure Active DIRECTORY (ad) etki alanı sanal makine uzantısını bir sanal makineye ekler.</span><span class="sxs-lookup"><span data-stu-id="eca44-106">The **Set-AzureRmVMADDomainExtension** cmdlet adds an Azure Active Directory (AD) domain virtual machine extension to a virtual machine.</span></span>
<span data-ttu-id="eca44-107">Bu uzantı, sanal makinenizin bir etki alanına katılmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="eca44-107">This extension lets your virtual machine join a domain.</span></span>

## <span data-ttu-id="eca44-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="eca44-108">EXAMPLES</span></span>

## <span data-ttu-id="eca44-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="eca44-109">PARAMETERS</span></span>

### <span data-ttu-id="eca44-110">-Credential</span><span class="sxs-lookup"><span data-stu-id="eca44-110">-Credential</span></span>
<span data-ttu-id="eca44-111">Sanal makinenin bir **PSCredential** nesnesi olarak Kullanıcı adını ve parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="eca44-111">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="eca44-112">Kimlik bilgilerini almak için Get-Credential cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="eca44-112">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="eca44-113">Daha fazla bilgi için yazın `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="eca44-113">For more information, type `Get-Help Get-Credential`.</span></span>

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

### <span data-ttu-id="eca44-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eca44-114">-DefaultProfile</span></span>
<span data-ttu-id="eca44-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="eca44-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eca44-116">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="eca44-116">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="eca44-117">Bu cmdlet 'in, uzantının ara sürümünün otomatik yükseltmesini devre dışı bırakacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="eca44-117">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

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

### <span data-ttu-id="eca44-118">-EtkiAlanıAdı</span><span class="sxs-lookup"><span data-stu-id="eca44-118">-DomainName</span></span>
<span data-ttu-id="eca44-119">Etki alanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="eca44-119">Specifies the name of the domain.</span></span>

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

### <span data-ttu-id="eca44-120">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="eca44-120">-ForceRerun</span></span>
<span data-ttu-id="eca44-121">Bu cmdlet 'in, uzantıyı kaldırıp yeniden yüklemeden sanal makinede aynı uzantı yapılandırmasını yeniden çalıştırmayı zortığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="eca44-121">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="eca44-122">Değer, geçerli değerden farklı olabilir.</span><span class="sxs-lookup"><span data-stu-id="eca44-122">The value can be any string different from the current value.</span></span>

<span data-ttu-id="eca44-123">ForceUpdateTag değiştirilirse, genel veya korumalı ayarlara yönelik güncelleştirmeler işleyici tarafından uygulanır.</span><span class="sxs-lookup"><span data-stu-id="eca44-123">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="eca44-124">-JoinOption</span><span class="sxs-lookup"><span data-stu-id="eca44-124">-JoinOption</span></span>
<span data-ttu-id="eca44-125">Katılma seçeneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="eca44-125">Specifies the join option.</span></span>

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

### <span data-ttu-id="eca44-126">-Konum</span><span class="sxs-lookup"><span data-stu-id="eca44-126">-Location</span></span>
<span data-ttu-id="eca44-127">Sanal makinenin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="eca44-127">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="eca44-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="eca44-128">-Name</span></span>
<span data-ttu-id="eca44-129">Eklenecek etki alanı uzantısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="eca44-129">Specifies the name of the domain extension to add.</span></span>

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

### <span data-ttu-id="eca44-130">-OUPath</span><span class="sxs-lookup"><span data-stu-id="eca44-130">-OUPath</span></span>
<span data-ttu-id="eca44-131">Etki alanı hesabı için bir kuruluş birimi (OU) belirtir.</span><span class="sxs-lookup"><span data-stu-id="eca44-131">Specifies an organizational unit (OU) for the domain account.</span></span>
<span data-ttu-id="eca44-132">KURULUŞ biriminin tam ayırt edici adını tırnak içine girin.</span><span class="sxs-lookup"><span data-stu-id="eca44-132">Enter the full distinguished name of the OU in quotation marks.</span></span>
<span data-ttu-id="eca44-133">Varsayılan değer, etki alanındaki makine nesnelerinin varsayılan OU 'dır.</span><span class="sxs-lookup"><span data-stu-id="eca44-133">The default value is the default OU for machine objects in the domain.</span></span>

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

### <span data-ttu-id="eca44-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eca44-134">-ResourceGroupName</span></span>
<span data-ttu-id="eca44-135">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="eca44-135">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="eca44-136">-Restart</span><span class="sxs-lookup"><span data-stu-id="eca44-136">-Restart</span></span>
<span data-ttu-id="eca44-137">Bu cmdlet 'in sanal makineyi yeniden başlattığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="eca44-137">Indicates that this cmdlet restarts the virtual machine.</span></span>
<span data-ttu-id="eca44-138">Değişikliğin etkili olması için genellikle yeniden başlatma gerekir.</span><span class="sxs-lookup"><span data-stu-id="eca44-138">A restart is often required to make the change effective.</span></span>

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

### <span data-ttu-id="eca44-139">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="eca44-139">-TypeHandlerVersion</span></span>
<span data-ttu-id="eca44-140">Etki alanı uzantısının sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="eca44-140">Specifies the version of the domain extension.</span></span>

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

### <span data-ttu-id="eca44-141">-VMName</span><span class="sxs-lookup"><span data-stu-id="eca44-141">-VMName</span></span>
<span data-ttu-id="eca44-142">Sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="eca44-142">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="eca44-143">-Onay</span><span class="sxs-lookup"><span data-stu-id="eca44-143">-Confirm</span></span>
<span data-ttu-id="eca44-144">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="eca44-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eca44-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eca44-145">-WhatIf</span></span>
<span data-ttu-id="eca44-146">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="eca44-146">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="eca44-147">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="eca44-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eca44-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eca44-148">CommonParameters</span></span>
<span data-ttu-id="eca44-149">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="eca44-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eca44-150">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eca44-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eca44-151">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="eca44-151">INPUTS</span></span>

### <span data-ttu-id="eca44-152">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="eca44-152">None</span></span>
<span data-ttu-id="eca44-153">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="eca44-153">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="eca44-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="eca44-154">OUTPUTS</span></span>

### <span data-ttu-id="eca44-155">Microsoft. Azure. Commands. COMPUTE. modeller. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="eca44-155">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="eca44-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="eca44-156">NOTES</span></span>

## <span data-ttu-id="eca44-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="eca44-157">RELATED LINKS</span></span>

[<span data-ttu-id="eca44-158">Get-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="eca44-158">Get-AzureRmVMADDomainExtension</span></span>](./Get-AzureRmVMADDomainExtension.md)
