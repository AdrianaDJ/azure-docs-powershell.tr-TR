---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 63BBDF98-75FC-4A44-9FD0-95AD21ED93A6
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/export-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Export-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Export-AzResourceGroup.md
ms.openlocfilehash: f1801aab91887b3dd0d6a9842c7d4a6de1988a88
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/08/2020
ms.locfileid: "93765226"
---
# <span data-ttu-id="52957-101">Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="52957-101">Export-AzResourceGroup</span></span>

## <span data-ttu-id="52957-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52957-102">SYNOPSIS</span></span>
<span data-ttu-id="52957-103">Kaynak grubu şablon olarak yakalar ve dosyaya kaydeder.</span><span class="sxs-lookup"><span data-stu-id="52957-103">Captures a resource group as a template and saves it to a file.</span></span>

## <span data-ttu-id="52957-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="52957-104">SYNTAX</span></span>

```
Export-AzResourceGroup -ResourceGroupName <String> [-Path <String>] [-IncludeParameterDefaultValue]
 [-IncludeComments] [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52957-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="52957-105">DESCRIPTION</span></span>
<span data-ttu-id="52957-106">**Export-AzResourceGroup** cmdlet 'i belirtilen kaynak grubunu şablon olarak yakalar ve bir JSON dosyasına kaydeder. Bu, kaynak grubunuzda daha önce bazı kaynakları oluşturmuş ve şablon destekli dağıtımları kullanmanın avantajlarından yararlanmak için kullanışlı olabilir.</span><span class="sxs-lookup"><span data-stu-id="52957-106">The **Export-AzResourceGroup** cmdlet captures the specified resource group as a template and saves it to a JSON file.This can be useful in scenarios where you have already created some resources in your resource group, and then want to leverage the benefits of using template backed deployments.</span></span>
<span data-ttu-id="52957-107">Bu cmdlet, kaynak grubunda var olan kaynaklarınız için şablon oluşturarak kolay bir başlangıç sağlar.</span><span class="sxs-lookup"><span data-stu-id="52957-107">This cmdlet gives you an easy start by generating the template for your existing resources in the resource group.</span></span>
<span data-ttu-id="52957-108">Bu cmdlet 'in şablonun bazı parçalarını oluşturamadığı bazı durumlar olabilir.</span><span class="sxs-lookup"><span data-stu-id="52957-108">There might be some cases where this cmdlet fails to generate some parts of the template.</span></span>
<span data-ttu-id="52957-109">Uyarı mesajları size başarısız olan kaynakları bildirir.</span><span class="sxs-lookup"><span data-stu-id="52957-109">Warning messages will inform you of the resources that failed.</span></span>
<span data-ttu-id="52957-110">Şablon, başarılı olan parçalar için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="52957-110">The template will still be generated for the parts that were successful.</span></span>

## <span data-ttu-id="52957-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="52957-111">EXAMPLES</span></span>

### <span data-ttu-id="52957-112">Örnek 1: kaynak grubunu dışarı aktarma</span><span class="sxs-lookup"><span data-stu-id="52957-112">Example 1: Export a resource group</span></span>
```
PS C:\>Export-AzResourceGroup -ResourceGroupName "TestGroup"
```

<span data-ttu-id="52957-113">Bu komut TestGroup adındaki kaynak grubunu şablon olarak yakalar ve geçerli dizindeki bir JSON dosyasına kaydeder.</span><span class="sxs-lookup"><span data-stu-id="52957-113">This command captures the resource group named TestGroup as a template, and saves it to a JSON file in the current directory.</span></span>

## <span data-ttu-id="52957-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="52957-114">PARAMETERS</span></span>

### <span data-ttu-id="52957-115">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="52957-115">-ApiVersion</span></span>
<span data-ttu-id="52957-116">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="52957-116">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="52957-117">Belirtilmezse, en son API sürümü kullanılır.</span><span class="sxs-lookup"><span data-stu-id="52957-117">If not specified, the latest API version is used.</span></span>

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

### <span data-ttu-id="52957-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52957-118">-DefaultProfile</span></span>
<span data-ttu-id="52957-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="52957-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="52957-120">-Force</span><span class="sxs-lookup"><span data-stu-id="52957-120">-Force</span></span>
<span data-ttu-id="52957-121">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="52957-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="52957-122">-Includecomments</span><span class="sxs-lookup"><span data-stu-id="52957-122">-IncludeComments</span></span>
<span data-ttu-id="52957-123">Bu işlemin şablonu açıklamalarla dışarı aktardığı anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="52957-123">Indicates that this operation exports the template with comments.</span></span>

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

### <span data-ttu-id="52957-124">-Includeparameterdefaultvalue</span><span class="sxs-lookup"><span data-stu-id="52957-124">-IncludeParameterDefaultValue</span></span>
<span data-ttu-id="52957-125">Bu işlemin varsayılan değer olan şablon parametresini dışarı aktardığı anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="52957-125">Indicates that this operation exports the template parameter with the default value.</span></span>

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

### <span data-ttu-id="52957-126">-Yol</span><span class="sxs-lookup"><span data-stu-id="52957-126">-Path</span></span>
<span data-ttu-id="52957-127">Şablon dosyasının çıkış yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="52957-127">Specifies the output path of the template file.</span></span>

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

### <span data-ttu-id="52957-128">-Pre-</span><span class="sxs-lookup"><span data-stu-id="52957-128">-Pre</span></span>
<span data-ttu-id="52957-129">Bu cmdlet 'in hangi API sürümünü kullanacağını otomatik olarak belirlerken sürüm öncesi API sürümlerini kullanacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="52957-129">Indicates that this cmdlet use pre-release API versions when automatically determining which API version to use.</span></span>

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

### <span data-ttu-id="52957-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52957-130">-ResourceGroupName</span></span>
<span data-ttu-id="52957-131">Dışarı aktarılacak kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="52957-131">Specifies the name of the resource group to export.</span></span>

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

### <span data-ttu-id="52957-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="52957-132">-Confirm</span></span>
<span data-ttu-id="52957-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="52957-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52957-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52957-134">-WhatIf</span></span>
<span data-ttu-id="52957-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="52957-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52957-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="52957-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52957-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52957-137">CommonParameters</span></span>
<span data-ttu-id="52957-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="52957-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52957-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52957-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52957-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="52957-140">INPUTS</span></span>

### <span data-ttu-id="52957-141">System. String</span><span class="sxs-lookup"><span data-stu-id="52957-141">System.String</span></span>

## <span data-ttu-id="52957-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="52957-142">OUTPUTS</span></span>

### <span data-ttu-id="52957-143">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="52957-143">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="52957-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="52957-144">NOTES</span></span>

## <span data-ttu-id="52957-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="52957-145">RELATED LINKS</span></span>

[<span data-ttu-id="52957-146">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="52957-146">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)


