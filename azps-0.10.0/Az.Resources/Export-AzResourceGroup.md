---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 63BBDF98-75FC-4A44-9FD0-95AD21ED93A6
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/export-Azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Export-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Export-AzResourceGroup.md
ms.openlocfilehash: 90ad1932a325aa79a4da2daa839a9c1d02ea72e6
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/08/2020
ms.locfileid: "94107370"
---
# <span data-ttu-id="bee65-101">Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="bee65-101">Export-AzResourceGroup</span></span>

## <span data-ttu-id="bee65-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bee65-102">SYNOPSIS</span></span>
<span data-ttu-id="bee65-103">Kaynak grubu şablon olarak yakalar ve dosyaya kaydeder.</span><span class="sxs-lookup"><span data-stu-id="bee65-103">Captures a resource group as a template and saves it to a file.</span></span>

## <span data-ttu-id="bee65-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bee65-104">SYNTAX</span></span>

```
Export-AzResourceGroup -ResourceGroupName <String> [-Path <String>] [-IncludeParameterDefaultValue]
 [-IncludeComments] [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bee65-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="bee65-105">DESCRIPTION</span></span>
<span data-ttu-id="bee65-106">**Export-AzResourceGroup** cmdlet 'i belirtilen kaynak grubunu şablon olarak yakalar ve bir JSON dosyasına kaydeder. Bu, kaynak grubunuzda daha önce bazı kaynakları oluşturmuş ve şablon destekli dağıtımları kullanmanın avantajlarından yararlanmak için kullanışlı olabilir.</span><span class="sxs-lookup"><span data-stu-id="bee65-106">The **Export-AzResourceGroup** cmdlet captures the specified resource group as a template and saves it to a JSON file.This can be useful in scenarios where you have already created some resources in your resource group, and then want to leverage the benefits of using template backed deployments.</span></span>
<span data-ttu-id="bee65-107">Bu cmdlet, kaynak grubunda var olan kaynaklarınız için şablon oluşturarak kolay bir başlangıç sağlar.</span><span class="sxs-lookup"><span data-stu-id="bee65-107">This cmdlet gives you an easy start by generating the template for your existing resources in the resource group.</span></span>
<span data-ttu-id="bee65-108">Bu cmdlet 'in şablonun bazı parçalarını oluşturamadığı bazı durumlar olabilir.</span><span class="sxs-lookup"><span data-stu-id="bee65-108">There might be some cases where this cmdlet fails to generate some parts of the template.</span></span>
<span data-ttu-id="bee65-109">Uyarı mesajları size başarısız olan kaynakları bildirir.</span><span class="sxs-lookup"><span data-stu-id="bee65-109">Warning messages will inform you of the resources that failed.</span></span>
<span data-ttu-id="bee65-110">Şablon, başarılı olan parçalar için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="bee65-110">The template will still be generated for the parts that were successful.</span></span>

## <span data-ttu-id="bee65-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bee65-111">EXAMPLES</span></span>

### <span data-ttu-id="bee65-112">Örnek 1: kaynak grubunu dışarı aktarma</span><span class="sxs-lookup"><span data-stu-id="bee65-112">Example 1: Export a resource group</span></span>
```
PS C:\>Export-AzResourceGroup -ResourceGroupName "TestGroup"
```

<span data-ttu-id="bee65-113">Bu komut TestGroup adındaki kaynak grubunu şablon olarak yakalar ve geçerli dizindeki bir JSON dosyasına kaydeder.</span><span class="sxs-lookup"><span data-stu-id="bee65-113">This command captures the resource group named TestGroup as a template, and saves it to a JSON file in the current directory.</span></span>

## <span data-ttu-id="bee65-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bee65-114">PARAMETERS</span></span>

### <span data-ttu-id="bee65-115">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="bee65-115">-ApiVersion</span></span>
<span data-ttu-id="bee65-116">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="bee65-116">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="bee65-117">Belirtilmezse, en son API sürümü kullanılır.</span><span class="sxs-lookup"><span data-stu-id="bee65-117">If not specified, the latest API version is used.</span></span>

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

### <span data-ttu-id="bee65-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bee65-118">-DefaultProfile</span></span>
<span data-ttu-id="bee65-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="bee65-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bee65-120">-Force</span><span class="sxs-lookup"><span data-stu-id="bee65-120">-Force</span></span>
<span data-ttu-id="bee65-121">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="bee65-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="bee65-122">-Includecomments</span><span class="sxs-lookup"><span data-stu-id="bee65-122">-IncludeComments</span></span>
<span data-ttu-id="bee65-123">Bu işlemin şablonu açıklamalarla dışarı aktardığı anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="bee65-123">Indicates that this operation exports the template with comments.</span></span>

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

### <span data-ttu-id="bee65-124">-Includeparameterdefaultvalue</span><span class="sxs-lookup"><span data-stu-id="bee65-124">-IncludeParameterDefaultValue</span></span>
<span data-ttu-id="bee65-125">Bu işlemin varsayılan değer olan şablon parametresini dışarı aktardığı anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="bee65-125">Indicates that this operation exports the template parameter with the default value.</span></span>

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

### <span data-ttu-id="bee65-126">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="bee65-126">-InformationAction</span></span>
<span data-ttu-id="bee65-127">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bee65-127">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="bee65-128">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="bee65-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="bee65-129">'A</span><span class="sxs-lookup"><span data-stu-id="bee65-129">Continue</span></span>
- <span data-ttu-id="bee65-130">Manıza</span><span class="sxs-lookup"><span data-stu-id="bee65-130">Ignore</span></span>
- <span data-ttu-id="bee65-131">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="bee65-131">Inquire</span></span>
- <span data-ttu-id="bee65-132">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="bee65-132">SilentlyContinue</span></span>
- <span data-ttu-id="bee65-133">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="bee65-133">Stop</span></span>
- <span data-ttu-id="bee65-134">Biliriz</span><span class="sxs-lookup"><span data-stu-id="bee65-134">Suspend</span></span>

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

### <span data-ttu-id="bee65-135">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="bee65-135">-InformationVariable</span></span>
<span data-ttu-id="bee65-136">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="bee65-136">Specifies an information variable.</span></span>

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

### <span data-ttu-id="bee65-137">-Yol</span><span class="sxs-lookup"><span data-stu-id="bee65-137">-Path</span></span>
<span data-ttu-id="bee65-138">Şablon dosyasının çıkış yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="bee65-138">Specifies the output path of the template file.</span></span>

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

### <span data-ttu-id="bee65-139">-Pre-</span><span class="sxs-lookup"><span data-stu-id="bee65-139">-Pre</span></span>
<span data-ttu-id="bee65-140">Bu cmdlet 'in hangi API sürümünü kullanacağını otomatik olarak belirlerken sürüm öncesi API sürümlerini kullanacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bee65-140">Indicates that this cmdlet use pre-release API versions when automatically determining which API version to use.</span></span>

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

### <span data-ttu-id="bee65-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bee65-141">-ResourceGroupName</span></span>
<span data-ttu-id="bee65-142">Dışarı aktarılacak kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bee65-142">Specifies the name of the resource group to export.</span></span>

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

### <span data-ttu-id="bee65-143">-Onay</span><span class="sxs-lookup"><span data-stu-id="bee65-143">-Confirm</span></span>
<span data-ttu-id="bee65-144">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bee65-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bee65-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bee65-145">-WhatIf</span></span>
<span data-ttu-id="bee65-146">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bee65-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bee65-147">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bee65-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bee65-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bee65-148">CommonParameters</span></span>
<span data-ttu-id="bee65-149">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bee65-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bee65-150">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bee65-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bee65-151">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bee65-151">INPUTS</span></span>

## <span data-ttu-id="bee65-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bee65-152">OUTPUTS</span></span>

## <span data-ttu-id="bee65-153">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bee65-153">NOTES</span></span>

## <span data-ttu-id="bee65-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bee65-154">RELATED LINKS</span></span>

[<span data-ttu-id="bee65-155">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="bee65-155">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)


