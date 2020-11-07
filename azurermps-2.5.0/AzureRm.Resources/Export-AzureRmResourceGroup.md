---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 63BBDF98-75FC-4A44-9FD0-95AD21ED93A6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/export-azurermresourcegroup
schema: 2.0.0
ms.openlocfilehash: a5390cd66e97f05e80f52685af6e43135ed64141
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939251"
---
# <span data-ttu-id="50bc5-101">Export-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="50bc5-101">Export-AzureRmResourceGroup</span></span>

## <span data-ttu-id="50bc5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50bc5-102">SYNOPSIS</span></span>
<span data-ttu-id="50bc5-103">Kaynak grubu şablon olarak yakalar ve dosyaya kaydeder.</span><span class="sxs-lookup"><span data-stu-id="50bc5-103">Captures a resource group as a template and saves it to a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="50bc5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="50bc5-104">SYNTAX</span></span>

```
Export-AzureRmResourceGroup -ResourceGroupName <String> [-Path <String>] [-IncludeParameterDefaultValue]
 [-IncludeComments] [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="50bc5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="50bc5-105">DESCRIPTION</span></span>
<span data-ttu-id="50bc5-106">**Export-AzureRmResourceGroup** cmdlet 'i belirtilen kaynak grubunu şablon olarak yakalar ve bir JSON dosyasına kaydeder. Bu, kaynak grubunuzda daha önce bazı kaynakları oluşturmuş ve şablon destekli dağıtımları kullanmanın avantajlarından yararlanmak için kullanışlı olabilir.</span><span class="sxs-lookup"><span data-stu-id="50bc5-106">The **Export-AzureRmResourceGroup** cmdlet captures the specified resource group as a template and saves it to a JSON file.This can be useful in scenarios where you have already created some resources in your resource group, and then want to leverage the benefits of using template backed deployments.</span></span>
<span data-ttu-id="50bc5-107">Bu cmdlet, kaynak grubunda var olan kaynaklarınız için şablon oluşturarak kolay bir başlangıç sağlar.</span><span class="sxs-lookup"><span data-stu-id="50bc5-107">This cmdlet gives you an easy start by generating the template for your existing resources in the resource group.</span></span>
<span data-ttu-id="50bc5-108">Bu cmdlet 'in şablonun bazı parçalarını oluşturamadığı bazı durumlar olabilir.</span><span class="sxs-lookup"><span data-stu-id="50bc5-108">There might be some cases where this cmdlet fails to generate some parts of the template.</span></span>
<span data-ttu-id="50bc5-109">Uyarı mesajları size başarısız olan kaynakları bildirir.</span><span class="sxs-lookup"><span data-stu-id="50bc5-109">Warning messages will inform you of the resources that failed.</span></span>
<span data-ttu-id="50bc5-110">Şablon, başarılı olan parçalar için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="50bc5-110">The template will still be generated for the parts that were successful.</span></span>

## <span data-ttu-id="50bc5-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="50bc5-111">EXAMPLES</span></span>

### <span data-ttu-id="50bc5-112">Örnek 1: kaynak grubunu dışarı aktarma</span><span class="sxs-lookup"><span data-stu-id="50bc5-112">Example 1: Export a resource group</span></span>
```
PS C:\>Export-AzureRmResourceGroup -ResourceGroupName "TestGroup"
```

<span data-ttu-id="50bc5-113">Bu komut TestGroup adındaki kaynak grubunu şablon olarak yakalar ve geçerli dizindeki bir JSON dosyasına kaydeder.</span><span class="sxs-lookup"><span data-stu-id="50bc5-113">This command captures the resource group named TestGroup as a template, and saves it to a JSON file in the current directory.</span></span>

## <span data-ttu-id="50bc5-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="50bc5-114">PARAMETERS</span></span>

### <span data-ttu-id="50bc5-115">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="50bc5-115">-ApiVersion</span></span>
<span data-ttu-id="50bc5-116">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="50bc5-116">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="50bc5-117">Belirtilmezse, en son API sürümü kullanılır.</span><span class="sxs-lookup"><span data-stu-id="50bc5-117">If not specified, the latest API version is used.</span></span>

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

### <span data-ttu-id="50bc5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50bc5-118">-DefaultProfile</span></span>
<span data-ttu-id="50bc5-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="50bc5-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="50bc5-120">-Force</span><span class="sxs-lookup"><span data-stu-id="50bc5-120">-Force</span></span>
<span data-ttu-id="50bc5-121">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="50bc5-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="50bc5-122">-Includecomments</span><span class="sxs-lookup"><span data-stu-id="50bc5-122">-IncludeComments</span></span>
<span data-ttu-id="50bc5-123">Bu işlemin şablonu açıklamalarla dışarı aktardığı anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="50bc5-123">Indicates that this operation exports the template with comments.</span></span>

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

### <span data-ttu-id="50bc5-124">-Includeparameterdefaultvalue</span><span class="sxs-lookup"><span data-stu-id="50bc5-124">-IncludeParameterDefaultValue</span></span>
<span data-ttu-id="50bc5-125">Bu işlemin varsayılan değer olan şablon parametresini dışarı aktardığı anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="50bc5-125">Indicates that this operation exports the template parameter with the default value.</span></span>

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

### <span data-ttu-id="50bc5-126">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="50bc5-126">-InformationAction</span></span>
<span data-ttu-id="50bc5-127">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="50bc5-127">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="50bc5-128">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="50bc5-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="50bc5-129">'A</span><span class="sxs-lookup"><span data-stu-id="50bc5-129">Continue</span></span>
- <span data-ttu-id="50bc5-130">Manıza</span><span class="sxs-lookup"><span data-stu-id="50bc5-130">Ignore</span></span>
- <span data-ttu-id="50bc5-131">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="50bc5-131">Inquire</span></span>
- <span data-ttu-id="50bc5-132">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="50bc5-132">SilentlyContinue</span></span>
- <span data-ttu-id="50bc5-133">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="50bc5-133">Stop</span></span>
- <span data-ttu-id="50bc5-134">Biliriz</span><span class="sxs-lookup"><span data-stu-id="50bc5-134">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50bc5-135">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="50bc5-135">-InformationVariable</span></span>
<span data-ttu-id="50bc5-136">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="50bc5-136">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50bc5-137">-Yol</span><span class="sxs-lookup"><span data-stu-id="50bc5-137">-Path</span></span>
<span data-ttu-id="50bc5-138">Şablon dosyasının çıkış yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="50bc5-138">Specifies the output path of the template file.</span></span>

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

### <span data-ttu-id="50bc5-139">-Pre-</span><span class="sxs-lookup"><span data-stu-id="50bc5-139">-Pre</span></span>
<span data-ttu-id="50bc5-140">Bu cmdlet 'in hangi API sürümünü kullanacağını otomatik olarak belirlerken sürüm öncesi API sürümlerini kullanacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="50bc5-140">Indicates that this cmdlet use pre-release API versions when automatically determining which API version to use.</span></span>

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

### <span data-ttu-id="50bc5-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50bc5-141">-ResourceGroupName</span></span>
<span data-ttu-id="50bc5-142">Dışarı aktarılacak kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="50bc5-142">Specifies the name of the resource group to export.</span></span>

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

### <span data-ttu-id="50bc5-143">-Onay</span><span class="sxs-lookup"><span data-stu-id="50bc5-143">-Confirm</span></span>
<span data-ttu-id="50bc5-144">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="50bc5-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50bc5-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50bc5-145">-WhatIf</span></span>
<span data-ttu-id="50bc5-146">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="50bc5-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50bc5-147">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="50bc5-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50bc5-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50bc5-148">CommonParameters</span></span>
<span data-ttu-id="50bc5-149">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="50bc5-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50bc5-150">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50bc5-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50bc5-151">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="50bc5-151">INPUTS</span></span>

## <span data-ttu-id="50bc5-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="50bc5-152">OUTPUTS</span></span>

## <span data-ttu-id="50bc5-153">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="50bc5-153">NOTES</span></span>

## <span data-ttu-id="50bc5-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="50bc5-154">RELATED LINKS</span></span>




