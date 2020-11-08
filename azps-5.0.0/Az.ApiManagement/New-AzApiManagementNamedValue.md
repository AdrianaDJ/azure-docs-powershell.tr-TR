---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementnamedvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementNamedValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementNamedValue.md
ms.openlocfilehash: 08e29c91e253c648b774e56d7e236accdd5fbff0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276929"
---
# <span data-ttu-id="2edd9-101">New-AzApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="2edd9-101">New-AzApiManagementNamedValue</span></span>

## <span data-ttu-id="2edd9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2edd9-102">SYNOPSIS</span></span>
<span data-ttu-id="2edd9-103">Yeni adlandırılan değer oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2edd9-103">Creates new Named Value.</span></span>

## <span data-ttu-id="2edd9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2edd9-104">SYNTAX</span></span>

```
New-AzApiManagementNamedValue -Context <PsApiManagementContext> [-NamedValueId <String>] -Name <String>
 -Value <String> [-Secret] [-Tag <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2edd9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2edd9-105">DESCRIPTION</span></span>
<span data-ttu-id="2edd9-106">**Yeni-Azapsananagementnamedvalue** cmdlet 'ı BIR Azure API Yönetimi **adı değeri** oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2edd9-106">The **New-AzApiManagementNamedValue** cmdlet creates an Azure API Management **Named Value**.</span></span>

## <span data-ttu-id="2edd9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2edd9-107">EXAMPLES</span></span>

### <span data-ttu-id="2edd9-108">Örnek 1: etiketleri içeren adlandırılmış bir değer oluşturma</span><span class="sxs-lookup"><span data-stu-id="2edd9-108">Example 1: Create a named value that includes tags</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> New-AzApiManagementNamedValue -Context $apimContext -NamedValueId "Property11" -Name "Property Name" -Value "Property Value" -Tags $Tags
```

<span data-ttu-id="2edd9-109">İlk komut $Tags değişkenine iki değer atar.</span><span class="sxs-lookup"><span data-stu-id="2edd9-109">The first command assigns two values to the $Tags variable.</span></span>
<span data-ttu-id="2edd9-110">İkinci komut, adlandırılmış bir değer oluşturur ve $Tags dizelere etiket olarak ekler.</span><span class="sxs-lookup"><span data-stu-id="2edd9-110">The second command creates a named value and assigns the strings in $Tags as tags on the property.</span></span>

### <span data-ttu-id="2edd9-111">Örnek 2: gizli değeri olan bir adlandırılmış değer oluşturma</span><span class="sxs-lookup"><span data-stu-id="2edd9-111">Example 2: Create a named value that has a secret value</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementNamedValue -Context $apimContext -NamedValueId "Property12" -Name "Secret Property" -Value "Secret Property Value" -Secret
```

<span data-ttu-id="2edd9-112">Bu komut şifrelenmiş bir değeri olan **adlandırılmış bir değer** oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2edd9-112">This command creates a **Named Value** that has a value that is encrypted.</span></span>

## <span data-ttu-id="2edd9-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2edd9-113">PARAMETERS</span></span>

### <span data-ttu-id="2edd9-114">-Context</span><span class="sxs-lookup"><span data-stu-id="2edd9-114">-Context</span></span>
<span data-ttu-id="2edd9-115">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="2edd9-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="2edd9-116">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="2edd9-116">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2edd9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2edd9-117">-DefaultProfile</span></span>
<span data-ttu-id="2edd9-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2edd9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2edd9-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="2edd9-119">-Name</span></span>
<span data-ttu-id="2edd9-120">Adlandırılmış değerin adı.</span><span class="sxs-lookup"><span data-stu-id="2edd9-120">Name of the named value.</span></span>
<span data-ttu-id="2edd9-121">Maksimum Uzunluk 100 karakterdir.</span><span class="sxs-lookup"><span data-stu-id="2edd9-121">Maximum length is 100 characters.</span></span>
<span data-ttu-id="2edd9-122">Yalnızca harf, rakam, nokta, çizgi ve alt çizgi karakterlerini içerebilir.</span><span class="sxs-lookup"><span data-stu-id="2edd9-122">It may contain only letters, digits, period, dash, and underscore characters.</span></span>
<span data-ttu-id="2edd9-123">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="2edd9-123">This parameter is required.</span></span>

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

### <span data-ttu-id="2edd9-124">Namedvalueıd</span><span class="sxs-lookup"><span data-stu-id="2edd9-124">-NamedValueId</span></span>
<span data-ttu-id="2edd9-125">Yeni adlandırılan değerin tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="2edd9-125">Identifier of new named value.</span></span>
<span data-ttu-id="2edd9-126">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="2edd9-126">This parameter is optional.</span></span>
<span data-ttu-id="2edd9-127">Belirtilmemişse,.</span><span class="sxs-lookup"><span data-stu-id="2edd9-127">If not specified will be generated.</span></span>

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

### <span data-ttu-id="2edd9-128">-Parola</span><span class="sxs-lookup"><span data-stu-id="2edd9-128">-Secret</span></span>
<span data-ttu-id="2edd9-129">Değerin gizli olup olmadığını ve şifrelenmesi gerektiğini belirler.</span><span class="sxs-lookup"><span data-stu-id="2edd9-129">Determines whether the value is a secret and should be encrypted or not.</span></span>
<span data-ttu-id="2edd9-130">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="2edd9-130">This parameter is optional.</span></span>
<span data-ttu-id="2edd9-131">Varsayılan değer: false.</span><span class="sxs-lookup"><span data-stu-id="2edd9-131">Default Value is false.</span></span>

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

### <span data-ttu-id="2edd9-132">Etiketli</span><span class="sxs-lookup"><span data-stu-id="2edd9-132">-Tag</span></span>
<span data-ttu-id="2edd9-133">Adlandırılan değer ile ilişkilendirilecek Etiketler.</span><span class="sxs-lookup"><span data-stu-id="2edd9-133">Tags to be associated with named value.</span></span>
<span data-ttu-id="2edd9-134">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="2edd9-134">This parameter is optional.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2edd9-135">-Değer</span><span class="sxs-lookup"><span data-stu-id="2edd9-135">-Value</span></span>
<span data-ttu-id="2edd9-136">Adlandırılmış değerin değeri.</span><span class="sxs-lookup"><span data-stu-id="2edd9-136">Value of the named value.</span></span>
<span data-ttu-id="2edd9-137">İlke ifadeleri içerebilir.</span><span class="sxs-lookup"><span data-stu-id="2edd9-137">Can contain policy expressions.</span></span>
<span data-ttu-id="2edd9-138">Maksimum uzunluk 1000 karakterdir.</span><span class="sxs-lookup"><span data-stu-id="2edd9-138">Maximum length is 1000 characters.</span></span>
<span data-ttu-id="2edd9-139">Boş veya yalnızca boşluklardan oluşamaz.</span><span class="sxs-lookup"><span data-stu-id="2edd9-139">It may not be empty or consist only of whitespace.</span></span>
<span data-ttu-id="2edd9-140">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="2edd9-140">This parameter is required.</span></span>

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

### <span data-ttu-id="2edd9-141">-Onay</span><span class="sxs-lookup"><span data-stu-id="2edd9-141">-Confirm</span></span>
<span data-ttu-id="2edd9-142">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2edd9-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2edd9-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2edd9-143">-WhatIf</span></span>
<span data-ttu-id="2edd9-144">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2edd9-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2edd9-145">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2edd9-145">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2edd9-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2edd9-146">CommonParameters</span></span>
<span data-ttu-id="2edd9-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2edd9-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2edd9-148">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="2edd9-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2edd9-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2edd9-149">INPUTS</span></span>

### <span data-ttu-id="2edd9-150">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="2edd9-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2edd9-151">System. String</span><span class="sxs-lookup"><span data-stu-id="2edd9-151">System.String</span></span>

### <span data-ttu-id="2edd9-152">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2edd9-152">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="2edd9-153">System. String []</span><span class="sxs-lookup"><span data-stu-id="2edd9-153">System.String[]</span></span>

## <span data-ttu-id="2edd9-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2edd9-154">OUTPUTS</span></span>

### <span data-ttu-id="2edd9-155">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementnamedvalue</span><span class="sxs-lookup"><span data-stu-id="2edd9-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValue</span></span>

## <span data-ttu-id="2edd9-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2edd9-156">NOTES</span></span>

## <span data-ttu-id="2edd9-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2edd9-157">RELATED LINKS</span></span>
