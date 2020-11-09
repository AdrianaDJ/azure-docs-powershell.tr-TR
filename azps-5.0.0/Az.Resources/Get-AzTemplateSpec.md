---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTemplateSpec.md
ms.openlocfilehash: be3a16707303016e22be8052721efcb35c608b3e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322903"
---
# <span data-ttu-id="18b5a-101">Get-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="18b5a-101">Get-AzTemplateSpec</span></span>

## <span data-ttu-id="18b5a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18b5a-102">SYNOPSIS</span></span>
<span data-ttu-id="18b5a-103">Şablon özelliklerinin alır veya listeler</span><span class="sxs-lookup"><span data-stu-id="18b5a-103">Gets or lists Template Specs</span></span>

## <span data-ttu-id="18b5a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="18b5a-104">SYNTAX</span></span>

### <span data-ttu-id="18b5a-105">ListTemplateSpecsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="18b5a-105">ListTemplateSpecsParameterSet (Default)</span></span>
```
Get-AzTemplateSpec [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="18b5a-106">GetTemplateSpecByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="18b5a-106">GetTemplateSpecByNameParameterSet</span></span>
```
Get-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="18b5a-107">Gettemplatespecbyıdparameterset</span><span class="sxs-lookup"><span data-stu-id="18b5a-107">GetTemplateSpecByIdParameterSet</span></span>
```
Get-AzTemplateSpec [[-Version] <String>] [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="18b5a-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="18b5a-108">DESCRIPTION</span></span>
<span data-ttu-id="18b5a-109">Bu cmdlet, bir abonelik/kaynak grubundaki şablon özelliklerinin listesini oluşturmak veya ad veya kimlik ile belirli bir şablon belirtimi almak için kullanılabilir. Ad/kimlik ile belirli bir şablon belirtimini alırken, belirli bir sürüm isteğe bağlı olarak, **-Version** parametresi aracılığıyla bir sürüm adı belirtilerek alınabilir.</span><span class="sxs-lookup"><span data-stu-id="18b5a-109">This cmdlet can be used to list Template Specs in a subscription/resource group or get a specific Template Spec by name or id. When getting a specific Template Spec by name/id a specific version can optionally be retrieved by specifying a version name through the **-Version** parameter.</span></span> <span data-ttu-id="18b5a-110">**-Version** kullanıldığında \* içinde yalnızca belirli sürüm ayrıntıları olacaktır *.* Döndürülen şablon belirtimi nesnesindeki sürümler.</span><span class="sxs-lookup"><span data-stu-id="18b5a-110">When **-Version** is used, only the specific version details will be present within \* *.Versions* on the returned Template Spec object.</span></span> <span data-ttu-id="18b5a-111">Bir şablon spec 'i Name/ID ile alırken belirli bir sürüm belirtilmemişse, tüm sürümler \* içinde yer alır *.* Döndürülen nesnenin sürümler özelliği.</span><span class="sxs-lookup"><span data-stu-id="18b5a-111">If no specific version is specified when retrieving a Template Spec by name/id, all versions will be present within the  \* *.Versions* property of the returned object.</span></span>

<span data-ttu-id="18b5a-112">**Not** : bir abonelik veya kaynak grubundaki tüm şablon özelliklerinin listesi *Sürümler "* özelliği *boş* olur.</span><span class="sxs-lookup"><span data-stu-id="18b5a-112">**Note** : When listing all Template Specs within a subscription or resource group, each returned Template Spec's *".Versions"* property will be *null*.</span></span> <span data-ttu-id="18b5a-113">Sürüm bilgileri yalnızca-Name veya-RESOURCEID parametreleri sağlandığında sunulur (örneğin: belirli bir şablon belirtimi/sürümü isteniyor).</span><span class="sxs-lookup"><span data-stu-id="18b5a-113">Version information is only included when -Name or -ResourceId parameters are provided (eg: you are requesting a specific template spec/version).</span></span>

## <span data-ttu-id="18b5a-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="18b5a-114">EXAMPLES</span></span>

### <span data-ttu-id="18b5a-115">Örnek 1: geçerli abonelikteki liste şablonu özellikleri</span><span class="sxs-lookup"><span data-stu-id="18b5a-115">Example 1: List Template Specs in current subscription</span></span>
```powershell
PS C:\> Get-AzTemplateSpec
```

<span data-ttu-id="18b5a-116">Geçerli abonelikteki tüm şablon özelliklerinin listesini listeler.</span><span class="sxs-lookup"><span data-stu-id="18b5a-116">Lists all Template Specs in the current subscription.</span></span>

### <span data-ttu-id="18b5a-117">Örnek 2: kaynak grubundaki şablon özelliklerinin listesi</span><span class="sxs-lookup"><span data-stu-id="18b5a-117">Example 2: List Template Specs in a resource group</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG'
```

<span data-ttu-id="18b5a-118">Geçerli aboneliğin tüm şablon özelliklerinin ' myRG ' kaynak grubunda listelenir.</span><span class="sxs-lookup"><span data-stu-id="18b5a-118">Lists all Template Specs in the resource group 'myRG' of the current subscription.</span></span>

### <span data-ttu-id="18b5a-119">Örnek 3: ada göre şablon belirtimi (tüm sürümlerle birlikte) alma</span><span class="sxs-lookup"><span data-stu-id="18b5a-119">Example 3: Get Template Spec (with all versions) by name</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec'
```

<span data-ttu-id="18b5a-120">' MyRG ' kaynak grubunun içindeki ' MyTemplateSpec ' adlı şablon belirtimi hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="18b5a-120">Gets information about the Template Spec named 'MyTemplateSpec' within the resource group 'myRG'.</span></span>

<span data-ttu-id="18b5a-121">**Not** : şablon belirtiminin tüm sürümleri " *.* , Return nesnesinin sürümü.</span><span class="sxs-lookup"><span data-stu-id="18b5a-121">**Note** : All of the Template Spec's versions will be present within the " *.Versions* " property of the return object.</span></span>

### <span data-ttu-id="18b5a-122">Örnek 4: ada göre şablon belirtimi (belirli bir sürüm) alma</span><span class="sxs-lookup"><span data-stu-id="18b5a-122">Example 4: Get Template Spec (specific version) by name</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec' -Version 'v1.0'
```

<span data-ttu-id="18b5a-123">' MyRG ' kaynak grubunda ' MyTemplateSpec ' adlı şablon belirtiminin sürümü hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="18b5a-123">Gets information about version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG'.</span></span>

<span data-ttu-id="18b5a-124">**Not** : *".* Döndürülen nesnenin sürümleri, yalnızca belirli bir sürümü içerir.</span><span class="sxs-lookup"><span data-stu-id="18b5a-124">**Note** : The *".Versions"* property of the returned object will contain only the specific version requested.</span></span>

### <span data-ttu-id="18b5a-125">Örnek 5: kaynak kimliğiyle şablon belirtimi (tüm sürümlerle birlikte) alma</span><span class="sxs-lookup"><span data-stu-id="18b5a-125">Example 5: Get Template Spec (with all versions) by resource id</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec'
```

<span data-ttu-id="18b5a-126">Abonelik alt kimliğindeki ' myRG ' kaynak grubunun içindeki ' MyTemplateSpec ' adlı şablon belirtimi hakkında bilgi alır \{ \} .</span><span class="sxs-lookup"><span data-stu-id="18b5a-126">Gets information about the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' of subscription \{subId\}.</span></span>

<span data-ttu-id="18b5a-127">**Not** : şablon belirtiminin tüm sürümleri " *.* , Return nesnesinin sürümü.</span><span class="sxs-lookup"><span data-stu-id="18b5a-127">**Note** : All of the Template Spec's versions will be present within the " *.Versions* " property of the return object.</span></span>

### <span data-ttu-id="18b5a-128">Örnek 6: kaynak kimliğiyle şablon belirtimi (belirli bir sürüm) alma</span><span class="sxs-lookup"><span data-stu-id="18b5a-128">Example 6: Get Template Spec (specific version) by resource id</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -Version 'v1.0'
```

<span data-ttu-id="18b5a-129">Abonelik alt kimliğindeki ' myRG ' kaynak grubunda ' MyTemplateSpec ' adlı şablon belirtiminin sürümü hakkında bilgi alır \{ \} .</span><span class="sxs-lookup"><span data-stu-id="18b5a-129">Gets information about version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' of subscription \{subId\}.</span></span>

<span data-ttu-id="18b5a-130">**Not** : *".* Döndürülen nesnenin sürümleri, yalnızca belirli bir sürümü içerir.</span><span class="sxs-lookup"><span data-stu-id="18b5a-130">**Note** : The *".Versions"* property of the returned object will contain only the specific version requested.</span></span>

## <span data-ttu-id="18b5a-131">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="18b5a-131">PARAMETERS</span></span>

### <span data-ttu-id="18b5a-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18b5a-132">-DefaultProfile</span></span>
<span data-ttu-id="18b5a-133">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="18b5a-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18b5a-134">-Ad</span><span class="sxs-lookup"><span data-stu-id="18b5a-134">-Name</span></span>
<span data-ttu-id="18b5a-135">Şablon belirtiminin adı.</span><span class="sxs-lookup"><span data-stu-id="18b5a-135">The name of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: GetTemplateSpecByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18b5a-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18b5a-136">-ResourceGroupName</span></span>
<span data-ttu-id="18b5a-137">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="18b5a-137">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ListTemplateSpecsParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetTemplateSpecByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18b5a-138">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="18b5a-138">-ResourceId</span></span>
<span data-ttu-id="18b5a-139">Şablon belirtiminin tam kaynak kimliği. örnek:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span><span class="sxs-lookup"><span data-stu-id="18b5a-139">The fully qualified resource Id of the template spec. Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span></span>

```yaml
Type: System.String
Parameter Sets: GetTemplateSpecByIdParameterSet
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18b5a-140">-Version</span><span class="sxs-lookup"><span data-stu-id="18b5a-140">-Version</span></span>
<span data-ttu-id="18b5a-141">Şablon belirtiminin sürümü.</span><span class="sxs-lookup"><span data-stu-id="18b5a-141">The version of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: GetTemplateSpecByNameParameterSet, GetTemplateSpecByIdParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18b5a-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18b5a-142">CommonParameters</span></span>
<span data-ttu-id="18b5a-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="18b5a-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18b5a-144">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="18b5a-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18b5a-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="18b5a-145">INPUTS</span></span>

### <span data-ttu-id="18b5a-146">System. String</span><span class="sxs-lookup"><span data-stu-id="18b5a-146">System.String</span></span>

## <span data-ttu-id="18b5a-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="18b5a-147">OUTPUTS</span></span>

### <span data-ttu-id="18b5a-148">Microsoft. Azure. Commands. ResourceManager. cmdlet. Sdkmodeller. PSTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="18b5a-148">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span></span>

## <span data-ttu-id="18b5a-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="18b5a-149">NOTES</span></span>

## <span data-ttu-id="18b5a-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="18b5a-150">RELATED LINKS</span></span>
