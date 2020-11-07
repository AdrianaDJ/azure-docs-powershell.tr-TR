---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 63BBDF98-75FC-4A44-9FD0-95AD21ED93A6
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/export-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Export-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Export-AzResourceGroup.md
ms.openlocfilehash: b249faa024206b14c0f3729ddc9214535c55c389
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/08/2020
ms.locfileid: "93940236"
---
# <span data-ttu-id="8c4d1-101">Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8c4d1-101">Export-AzResourceGroup</span></span>

## <span data-ttu-id="8c4d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c4d1-102">SYNOPSIS</span></span>
<span data-ttu-id="8c4d1-103">Kaynak grubu şablon olarak yakalar ve dosyaya kaydeder.</span><span class="sxs-lookup"><span data-stu-id="8c4d1-103">Captures a resource group as a template and saves it to a file.</span></span>

## <span data-ttu-id="8c4d1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8c4d1-104">SYNTAX</span></span>

```
Export-AzResourceGroup -ResourceGroupName <String> [-Path <String>] [-IncludeParameterDefaultValue]
 [-IncludeComments] [-SkipResourceNameParameterization] [-SkipAllParameterization]
 [-Resource <String[]>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c4d1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8c4d1-105">DESCRIPTION</span></span>
<span data-ttu-id="8c4d1-106">**Export-AzResourceGroup** cmdlet 'i belirtilen kaynak grubunu şablon olarak yakalar ve bir JSON dosyasına kaydeder. Bu, kaynak grubunuzda daha önce bazı kaynakları oluşturmuş ve şablon destekli dağıtımları kullanmanın avantajlarından yararlanmak için kullanışlı olabilir.</span><span class="sxs-lookup"><span data-stu-id="8c4d1-106">The **Export-AzResourceGroup** cmdlet captures the specified resource group as a template and saves it to a JSON file.This can be useful in scenarios where you have already created some resources in your resource group, and then want to leverage the benefits of using template backed deployments.</span></span>
<span data-ttu-id="8c4d1-107">Bu cmdlet, kaynak grubunda var olan kaynaklarınız için şablon oluşturarak kolay bir başlangıç sağlar.</span><span class="sxs-lookup"><span data-stu-id="8c4d1-107">This cmdlet gives you an easy start by generating the template for your existing resources in the resource group.</span></span>
<span data-ttu-id="8c4d1-108">Bu cmdlet 'in şablonun bazı parçalarını oluşturamadığı bazı durumlar olabilir.</span><span class="sxs-lookup"><span data-stu-id="8c4d1-108">There might be some cases where this cmdlet fails to generate some parts of the template.</span></span>
<span data-ttu-id="8c4d1-109">Uyarı mesajları size başarısız olan kaynakları bildirir.</span><span class="sxs-lookup"><span data-stu-id="8c4d1-109">Warning messages will inform you of the resources that failed.</span></span>
<span data-ttu-id="8c4d1-110">Şablon, başarılı olan parçalar için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="8c4d1-110">The template will still be generated for the parts that were successful.</span></span>

## <span data-ttu-id="8c4d1-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8c4d1-111">EXAMPLES</span></span>

### <span data-ttu-id="8c4d1-112">Örnek 1: kaynak grubunu dışarı aktarma</span><span class="sxs-lookup"><span data-stu-id="8c4d1-112">Example 1: Export a resource group</span></span>
```
PS C:\>Export-AzResourceGroup -ResourceGroupName "TestGroup"
```

<span data-ttu-id="8c4d1-113">Bu komut TestGroup adındaki kaynak grubunu şablon olarak yakalar ve geçerli dizindeki bir JSON dosyasına kaydeder.</span><span class="sxs-lookup"><span data-stu-id="8c4d1-113">This command captures the resource group named TestGroup as a template, and saves it to a JSON file in the current directory.</span></span>

### <span data-ttu-id="8c4d1-114">Örnek 2: kaynak grubundan tek bir kaynak dışarı aktarma</span><span class="sxs-lookup"><span data-stu-id="8c4d1-114">Example 2: Export a single resource from a resource group</span></span>
```
PS C:\>Export-AzResourceGroup -ResourceGroupName "TestGroup" -Resource "/subscriptions/5f43547b-1d2d-4a3e-ace4-88d4b600d568/resourceGroups/TestGroup/providers/Microsoft.Compute/virtualMachines/TestVirtualMachine"
```

<span data-ttu-id="8c4d1-115">Bu komut "TestGroup" adlı sanal makine kaynağını "TestGroup" kaynak grubundan şablon olarak yakalar ve geçerli dizindeki bir JSON dosyasına kaydeder.</span><span class="sxs-lookup"><span data-stu-id="8c4d1-115">This command captures the Virtual Machine resource named "TestVirtualMachine" from the "TestGroup" resource group as a template, and saves it to a JSON file in the current directory.</span></span>

### <span data-ttu-id="8c4d1-116">Örnek 3: kaynak grubundan kaynak seçimini dışarı aktarma</span><span class="sxs-lookup"><span data-stu-id="8c4d1-116">Example 3: Export a selection of resources from a resource group</span></span>
```
PS C:\>Export-AzResourceGroup -ResourceGroupName "TestGroup" -SkipAllParameterization -Resource @(
  "/subscriptions/5f43547b-1d2d-4a3e-ace4-88d4b600d568/resourceGroups/TestGroup/providers/Microsoft.Compute/virtualMachines/TestVm",
  "/subscriptions/5f43547b-1d2d-4a3e-ace4-88d4b600d568/resourceGroups/TestGroup/providers/Microsoft.Network/networkInterfaces/TestNic"
)
```

<span data-ttu-id="8c4d1-117">Bu komut, "TestGroup" kaynak grubundaki iki kaynağı şablon olarak yakalar ve geçerli dizindeki bir JSON dosyasına kaydeder.</span><span class="sxs-lookup"><span data-stu-id="8c4d1-117">This command captures two resources from the "TestGroup" resource group as a template, and saves it to a JSON file in the current directory.</span></span> <span data-ttu-id="8c4d1-118">Oluşturulan şablonda oluşturulmuş parametre bulunmaz.</span><span class="sxs-lookup"><span data-stu-id="8c4d1-118">The generated template will not contain any generated parameters.</span></span>

## <span data-ttu-id="8c4d1-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8c4d1-119">PARAMETERS</span></span>

### <span data-ttu-id="8c4d1-120">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="8c4d1-120">-ApiVersion</span></span>
<span data-ttu-id="8c4d1-121">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="8c4d1-121">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="8c4d1-122">Belirtilmezse, en son API sürümü kullanılır.</span><span class="sxs-lookup"><span data-stu-id="8c4d1-122">If not specified, the latest API version is used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c4d1-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c4d1-123">-DefaultProfile</span></span>
<span data-ttu-id="8c4d1-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="8c4d1-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8c4d1-125">-Force</span><span class="sxs-lookup"><span data-stu-id="8c4d1-125">-Force</span></span>
<span data-ttu-id="8c4d1-126">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="8c4d1-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8c4d1-127">-Includecomments</span><span class="sxs-lookup"><span data-stu-id="8c4d1-127">-IncludeComments</span></span>
<span data-ttu-id="8c4d1-128">Bu işlemin şablonu açıklamalarla dışarı aktardığı anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="8c4d1-128">Indicates that this operation exports the template with comments.</span></span>

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

### <span data-ttu-id="8c4d1-129">-Includeparameterdefaultvalue</span><span class="sxs-lookup"><span data-stu-id="8c4d1-129">-IncludeParameterDefaultValue</span></span>
<span data-ttu-id="8c4d1-130">Bu işlemin varsayılan değer olan şablon parametresini dışarı aktardığı anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="8c4d1-130">Indicates that this operation exports the template parameter with the default value.</span></span>

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

### <span data-ttu-id="8c4d1-131">-Yol</span><span class="sxs-lookup"><span data-stu-id="8c4d1-131">-Path</span></span>
<span data-ttu-id="8c4d1-132">Şablon dosyasının çıkış yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="8c4d1-132">Specifies the output path of the template file.</span></span>

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

### <span data-ttu-id="8c4d1-133">-Pre-</span><span class="sxs-lookup"><span data-stu-id="8c4d1-133">-Pre</span></span>
<span data-ttu-id="8c4d1-134">Bu cmdlet 'in hangi API sürümünü kullanacağını otomatik olarak belirlerken sürüm öncesi API sürümlerini kullanacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8c4d1-134">Indicates that this cmdlet use pre-release API versions when automatically determining which API version to use.</span></span>

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

### <span data-ttu-id="8c4d1-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c4d1-135">-ResourceGroupName</span></span>
<span data-ttu-id="8c4d1-136">Dışarı aktarılacak kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8c4d1-136">Specifies the name of the resource group to export.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c4d1-137">-Kaynak</span><span class="sxs-lookup"><span data-stu-id="8c4d1-137">-Resource</span></span>
<span data-ttu-id="8c4d1-138">Sonuçları filtrelemek için Resourceıds listesi.</span><span class="sxs-lookup"><span data-stu-id="8c4d1-138">A list of resourceIds to filter the results by.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c4d1-139">-Skipallparametreleme</span><span class="sxs-lookup"><span data-stu-id="8c4d1-139">-SkipAllParameterization</span></span>
<span data-ttu-id="8c4d1-140">Tüm parametrelemeyi atlayın.</span><span class="sxs-lookup"><span data-stu-id="8c4d1-140">Skip all parameterization.</span></span>

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

### <span data-ttu-id="8c4d1-141">-Skipresourcenameparameterbir</span><span class="sxs-lookup"><span data-stu-id="8c4d1-141">-SkipResourceNameParameterization</span></span>
<span data-ttu-id="8c4d1-142">Kaynak adı parametrelemeyi atlayın.</span><span class="sxs-lookup"><span data-stu-id="8c4d1-142">Skip resource name parameterization.</span></span>

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

### <span data-ttu-id="8c4d1-143">-Onay</span><span class="sxs-lookup"><span data-stu-id="8c4d1-143">-Confirm</span></span>
<span data-ttu-id="8c4d1-144">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8c4d1-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c4d1-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c4d1-145">-WhatIf</span></span>
<span data-ttu-id="8c4d1-146">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8c4d1-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c4d1-147">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8c4d1-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c4d1-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c4d1-148">CommonParameters</span></span>
<span data-ttu-id="8c4d1-149">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8c4d1-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c4d1-150">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="8c4d1-150">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c4d1-151">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8c4d1-151">INPUTS</span></span>

### <span data-ttu-id="8c4d1-152">System. String</span><span class="sxs-lookup"><span data-stu-id="8c4d1-152">System.String</span></span>

## <span data-ttu-id="8c4d1-153">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8c4d1-153">OUTPUTS</span></span>

### <span data-ttu-id="8c4d1-154">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="8c4d1-154">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="8c4d1-155">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8c4d1-155">NOTES</span></span>

## <span data-ttu-id="8c4d1-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8c4d1-156">RELATED LINKS</span></span>

[<span data-ttu-id="8c4d1-157">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8c4d1-157">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)


