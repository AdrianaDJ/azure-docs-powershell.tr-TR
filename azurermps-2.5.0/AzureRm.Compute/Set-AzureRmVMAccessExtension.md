---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D93666EC-C252-4E3B-B311-50B6EEA6D4BF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmaccessextension
schema: 2.0.0
ms.openlocfilehash: 069b98f585d606ade255cfecd223be4a074d8316
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939567"
---
# <span data-ttu-id="d7576-101">Set-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="d7576-101">Set-AzureRmVMAccessExtension</span></span>

## <span data-ttu-id="d7576-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7576-102">SYNOPSIS</span></span>
<span data-ttu-id="d7576-103">Sanal makineye VMAccess uzantısını ekler.</span><span class="sxs-lookup"><span data-stu-id="d7576-103">Adds the VMAccess extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7576-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d7576-104">SYNTAX</span></span>

```
Set-AzureRmVMAccessExtension [-Credential <PSCredential>] [-ResourceGroupName] <String> [-VMName] <String>
 [-Name <String>] [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion]
 [-ForceRerun <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7576-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d7576-105">DESCRIPTION</span></span>
<span data-ttu-id="d7576-106">**Set-Azurermvmaccessextenma** cmdlet 'i sanal makine erişimi (VMAccess) sanal makine VMAccess uzantısını bir sanal makineye ekler.</span><span class="sxs-lookup"><span data-stu-id="d7576-106">The **Set-AzureRmVMAccessExtension** cmdlet adds the Virtual Machine Access (VMAccess) Virtual Machine VMAccess Extension to a virtual machine.</span></span> <span data-ttu-id="d7576-107">VMAccess uzantısı geçici bir parola ayarlamak için kullanılabilir ve bu, makinede oturum açıldıktan sonra hemen değiştirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="d7576-107">VMAccess Extension can be used to set a temporary password and this should be immediately changed it after logging into the machine.</span></span>

## <span data-ttu-id="d7576-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d7576-108">EXAMPLES</span></span>

### <span data-ttu-id="d7576-109">Örnek 1: VMAccess uzantısı ekleme</span><span class="sxs-lookup"><span data-stu-id="d7576-109">Example 1: Add a VMAccess extension</span></span>
```
PS C:\> Set-AzureRmVMAccessExtension -ResourceGroupName "ResrouceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "2.0" -UserName "PFuller" -Password "Password"
```

<span data-ttu-id="d7576-110">Bu komut, ResrouceGroup11 'da VirtualMachine07 adındaki sanal makine için bir VMAccess uzantısı ekler.</span><span class="sxs-lookup"><span data-stu-id="d7576-110">This command adds a VMAccess extension for the virtual machine named VirtualMachine07 in ResrouceGroup11.</span></span>
<span data-ttu-id="d7576-111">Komut, VMAccess için ad ve tür işleyicisi sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="d7576-111">The command specifies the name and type handler version for VMAccess.</span></span>

## <span data-ttu-id="d7576-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d7576-112">PARAMETERS</span></span>

### <span data-ttu-id="d7576-113">-Credential</span><span class="sxs-lookup"><span data-stu-id="d7576-113">-Credential</span></span>
<span data-ttu-id="d7576-114">Sanal makinenin bir **PSCredential** nesnesi olarak Kullanıcı adını ve parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d7576-114">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="d7576-115">Kimlik bilgilerini almak için Get-Credential cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="d7576-115">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="d7576-116">Daha fazla bilgi için yazın `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="d7576-116">For more information, type `Get-Help Get-Credential`.</span></span>

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

### <span data-ttu-id="d7576-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7576-117">-DefaultProfile</span></span>
<span data-ttu-id="d7576-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d7576-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7576-119">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="d7576-119">-DisableAutoUpgradeMinorVersion</span></span>
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

### <span data-ttu-id="d7576-120">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="d7576-120">-ForceRerun</span></span>
<span data-ttu-id="d7576-121">Bu cmdlet 'in, uzantıyı kaldırıp yeniden yüklemeden sanal makinede aynı uzantı yapılandırmasını yeniden çalıştırmayı zortığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d7576-121">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="d7576-122">Değer, geçerli değerden farklı olabilir.</span><span class="sxs-lookup"><span data-stu-id="d7576-122">The value can be any string different from the current value.</span></span>

<span data-ttu-id="d7576-123">ForceUpdateTag değiştirilirse, genel veya korumalı ayarlara yönelik güncelleştirmeler işleyici tarafından uygulanır.</span><span class="sxs-lookup"><span data-stu-id="d7576-123">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="d7576-124">-Konum</span><span class="sxs-lookup"><span data-stu-id="d7576-124">-Location</span></span>
<span data-ttu-id="d7576-125">Sanal makinenin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="d7576-125">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="d7576-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="d7576-126">-Name</span></span>
<span data-ttu-id="d7576-127">Bu cmdlet 'in eklediği uzantının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d7576-127">Specifies the name of the extension that this cmdlet adds.</span></span>

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

### <span data-ttu-id="d7576-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7576-128">-ResourceGroupName</span></span>
<span data-ttu-id="d7576-129">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d7576-129">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="d7576-130">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="d7576-130">-TypeHandlerVersion</span></span>
<span data-ttu-id="d7576-131">Bu sanal makine için kullanılacak uzantının sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="d7576-131">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="d7576-132">Sürümü edinmek için, *tür* parametresinde Microsoft. *PublisherName* parametresi ve VMAccessAgent değerini içeren Get-AzureRmVMExtensionImage cmdlet 'ini çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="d7576-132">To obtain the version, run the Get-AzureRmVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span>

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

### <span data-ttu-id="d7576-133">-VMName</span><span class="sxs-lookup"><span data-stu-id="d7576-133">-VMName</span></span>
<span data-ttu-id="d7576-134">Sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d7576-134">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="d7576-135">Bu cmdlet, bu parametrenin belirttiği sanal makine için VMAccess öğesini ekler.</span><span class="sxs-lookup"><span data-stu-id="d7576-135">This cmdlet adds VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="d7576-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="d7576-136">-Confirm</span></span>
<span data-ttu-id="d7576-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d7576-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7576-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7576-138">-WhatIf</span></span>
<span data-ttu-id="d7576-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d7576-139">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="d7576-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d7576-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7576-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7576-141">CommonParameters</span></span>
<span data-ttu-id="d7576-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d7576-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7576-143">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7576-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7576-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d7576-144">INPUTS</span></span>

### <span data-ttu-id="d7576-145">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="d7576-145">None</span></span>
<span data-ttu-id="d7576-146">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="d7576-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d7576-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d7576-147">OUTPUTS</span></span>

### <span data-ttu-id="d7576-148">Microsoft. Azure. Commands. COMPUTE. modeller. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="d7576-148">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="d7576-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d7576-149">NOTES</span></span>

## <span data-ttu-id="d7576-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d7576-150">RELATED LINKS</span></span>

[<span data-ttu-id="d7576-151">Get-Azurermvmaccessextenma</span><span class="sxs-lookup"><span data-stu-id="d7576-151">Get-AzureRmVMAccessExtension</span></span>](./Get-AzureRmVMAccessExtension.md)

[<span data-ttu-id="d7576-152">Remove-Azurermvmaccessextenma</span><span class="sxs-lookup"><span data-stu-id="d7576-152">Remove-AzureRmVMAccessExtension</span></span>](./Remove-AzureRmVMAccessExtension.md)

[<span data-ttu-id="d7576-153">Set-Azurermvmexgeri</span><span class="sxs-lookup"><span data-stu-id="d7576-153">Set-AzureRmVMExtension</span></span>](./Set-AzureRmVMExtension.md)

[<span data-ttu-id="d7576-154">Get-Azurermvmextensionımage</span><span class="sxs-lookup"><span data-stu-id="d7576-154">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)


