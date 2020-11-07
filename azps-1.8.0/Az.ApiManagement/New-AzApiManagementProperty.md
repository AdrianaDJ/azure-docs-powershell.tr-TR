---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A91F93D3-B8C7-4328-A049-AB9877C1166C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementProperty.md
ms.openlocfilehash: d54665b767d10edde564450ecfcdd467b784dd8b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917844"
---
# <span data-ttu-id="e0472-101">New-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="e0472-101">New-AzApiManagementProperty</span></span>

## <span data-ttu-id="e0472-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0472-102">SYNOPSIS</span></span>
<span data-ttu-id="e0472-103">Yeni özellik oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e0472-103">Creates a new Property.</span></span>

## <span data-ttu-id="e0472-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e0472-104">SYNTAX</span></span>

```
New-AzApiManagementProperty -Context <PsApiManagementContext> [-PropertyId <String>] -Name <String>
 -Value <String> [-Secret] [-Tag <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0472-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e0472-105">DESCRIPTION</span></span>
<span data-ttu-id="e0472-106">**Yeni-Azapsananagementproperty** cmdlet 'ı BIR Azure API Yönetim **özelliği** oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e0472-106">The **New-AzApiManagementProperty** cmdlet creates an Azure API Management **Property**.</span></span>

## <span data-ttu-id="e0472-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e0472-107">EXAMPLES</span></span>

### <span data-ttu-id="e0472-108">Örnek 1: etiketleri içeren özellik oluşturma</span><span class="sxs-lookup"><span data-stu-id="e0472-108">Example 1: Create a property that includes tags</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> New-AzApiManagementProperty -Context $apimContext -PropertyId "Property11" -Name "Property Name" -Value "Property Value" -Tags $Tags
```

<span data-ttu-id="e0472-109">İlk komut $Tags değişkenine iki değer atar.</span><span class="sxs-lookup"><span data-stu-id="e0472-109">The first command assigns two values to the $Tags variable.</span></span>
<span data-ttu-id="e0472-110">İkinci komut bir özellik oluşturur ve $Tags dizelere etiket olarak atar.</span><span class="sxs-lookup"><span data-stu-id="e0472-110">The second command creates a property and assigns the strings in $Tags as tags on the property.</span></span>

### <span data-ttu-id="e0472-111">Örnek 2: gizli değeri olan bir özellik oluşturma</span><span class="sxs-lookup"><span data-stu-id="e0472-111">Example 2: Create a property that has a secret value</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementProperty -Context $apimContext -PropertyId "Property12" -Name "Secret Property -Value "Secret Property Value" -Secret
```

<span data-ttu-id="e0472-112">Bu komut şifrelenmiş bir değer içeren bir **özellik** oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e0472-112">This command creates a **Property** that has a value that is encrypted.</span></span>

## <span data-ttu-id="e0472-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e0472-113">PARAMETERS</span></span>

### <span data-ttu-id="e0472-114">-Context</span><span class="sxs-lookup"><span data-stu-id="e0472-114">-Context</span></span>
<span data-ttu-id="e0472-115">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e0472-115">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0472-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0472-116">-DefaultProfile</span></span>
<span data-ttu-id="e0472-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e0472-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e0472-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="e0472-118">-Name</span></span>
<span data-ttu-id="e0472-119">Bu cmdlet 'in oluşturduğu özelliğin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e0472-119">Specifies the name of the property that this cmdlet creates.</span></span>
<span data-ttu-id="e0472-120">Maksimum Uzunluk 100 karakterdir.</span><span class="sxs-lookup"><span data-stu-id="e0472-120">Maximum length is 100 characters.</span></span>
<span data-ttu-id="e0472-121">Adlar yalnızca harf, rakam, nokta, çizgi ve alt çizgi karakterlerini içerir.</span><span class="sxs-lookup"><span data-stu-id="e0472-121">Names contain only letters, digits, period, dash, and underscore characters.</span></span>

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

### <span data-ttu-id="e0472-122">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="e0472-122">-PropertyId</span></span>
<span data-ttu-id="e0472-123">Özelliğin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="e0472-123">Specifies an ID for the property.</span></span>
<span data-ttu-id="e0472-124">Maksimum uzunluk 256 karakterdir.</span><span class="sxs-lookup"><span data-stu-id="e0472-124">Maximum length is 256 characters.</span></span>
<span data-ttu-id="e0472-125">KIMLIK belirtmezseniz, bu cmdlet bir tane oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e0472-125">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="e0472-126">-Parola</span><span class="sxs-lookup"><span data-stu-id="e0472-126">-Secret</span></span>
<span data-ttu-id="e0472-127">Özellik değerinin gizli olduğunu ve şifrelenmesi gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e0472-127">Indicates that the property value is a secret and should be encrypted.</span></span>

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

### <span data-ttu-id="e0472-128">Etiketli</span><span class="sxs-lookup"><span data-stu-id="e0472-128">-Tag</span></span>
<span data-ttu-id="e0472-129">Özellik ile ilişkilendirilecek Etiketler.</span><span class="sxs-lookup"><span data-stu-id="e0472-129">Tags to be associated with Property.</span></span> <span data-ttu-id="e0472-130">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="e0472-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="e0472-131">-Değer</span><span class="sxs-lookup"><span data-stu-id="e0472-131">-Value</span></span>
<span data-ttu-id="e0472-132">Özellik için bir değer belirtir.</span><span class="sxs-lookup"><span data-stu-id="e0472-132">Specifies a value for the property.</span></span>
<span data-ttu-id="e0472-133">Bu değer ilke ifadeleri içerebilir.</span><span class="sxs-lookup"><span data-stu-id="e0472-133">This value can contain policy expressions.</span></span>
<span data-ttu-id="e0472-134">Maksimum uzunluk 1000 karakterdir.</span><span class="sxs-lookup"><span data-stu-id="e0472-134">Maximum length is 1000 characters.</span></span>
<span data-ttu-id="e0472-135">Değer boş olamaz veya yalnızca boşluklardan oluşamaz.</span><span class="sxs-lookup"><span data-stu-id="e0472-135">The value may not be empty or consist only of whitespace.</span></span>

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

### <span data-ttu-id="e0472-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0472-136">CommonParameters</span></span>
<span data-ttu-id="e0472-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e0472-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0472-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0472-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0472-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e0472-139">INPUTS</span></span>

### <span data-ttu-id="e0472-140">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="e0472-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e0472-141">System. String</span><span class="sxs-lookup"><span data-stu-id="e0472-141">System.String</span></span>

### <span data-ttu-id="e0472-142">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e0472-142">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="e0472-143">System. String []</span><span class="sxs-lookup"><span data-stu-id="e0472-143">System.String[]</span></span>

## <span data-ttu-id="e0472-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e0472-144">OUTPUTS</span></span>

### <span data-ttu-id="e0472-145">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementproperty</span><span class="sxs-lookup"><span data-stu-id="e0472-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="e0472-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e0472-146">NOTES</span></span>

## <span data-ttu-id="e0472-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e0472-147">RELATED LINKS</span></span>

[<span data-ttu-id="e0472-148">Remove-Azapsananagementproperty</span><span class="sxs-lookup"><span data-stu-id="e0472-148">Remove-AzApiManagementProperty</span></span>](./Remove-AzApiManagementProperty.md)

[<span data-ttu-id="e0472-149">Set-Azapsananagementözelliği</span><span class="sxs-lookup"><span data-stu-id="e0472-149">Set-AzApiManagementProperty</span></span>](./Set-AzApiManagementProperty.md)


