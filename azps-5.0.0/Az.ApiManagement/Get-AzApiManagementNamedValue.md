---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementnamedvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValue.md
ms.openlocfilehash: 8d6d7174278d1f997c6a62e75eec4958f75b1d6c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324073"
---
# <span data-ttu-id="293da-101">Get-AzApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="293da-101">Get-AzApiManagementNamedValue</span></span>

## <span data-ttu-id="293da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="293da-102">SYNOPSIS</span></span>
<span data-ttu-id="293da-103">Bir listeyi veya belirli bir adlandırılmış değeri alır.</span><span class="sxs-lookup"><span data-stu-id="293da-103">Gets a list or a particular Named Value.</span></span>

## <span data-ttu-id="293da-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="293da-104">SYNTAX</span></span>

### <span data-ttu-id="293da-105">GetAllNamedValues (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="293da-105">GetAllNamedValues (Default)</span></span>
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="293da-106">Getbynamedvalueıd</span><span class="sxs-lookup"><span data-stu-id="293da-106">GetByNamedValueId</span></span>
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-NamedValueId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="293da-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="293da-107">GetByName</span></span>
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="293da-108">GetByTag</span><span class="sxs-lookup"><span data-stu-id="293da-108">GetByTag</span></span>
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-Tag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="293da-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="293da-109">DESCRIPTION</span></span>
<span data-ttu-id="293da-110">**Get-Azapsananagementnamedvalue** cmdlet 'i, bir liste veya belirli bir adlandırılmış değeri alır.</span><span class="sxs-lookup"><span data-stu-id="293da-110">The **Get-AzApiManagementNamedValue** cmdlet gets a list or a particular named value.</span></span>
<span data-ttu-id="293da-111">Değer parola olarak işaretlenmişse, değer, sonuç ayrıntılarına dahil olmaz.</span><span class="sxs-lookup"><span data-stu-id="293da-111">Value will not be included into result details if the named value marked as a secret.</span></span> <span data-ttu-id="293da-112">Gizli değer almak için **Get-Azapsananagementnamedvaluesecretvalue** seçeneğini kullanın.</span><span class="sxs-lookup"><span data-stu-id="293da-112">To get secret value, use **Get-AzApiManagementNamedValueSecretValue**.</span></span>

## <span data-ttu-id="293da-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="293da-113">EXAMPLES</span></span>

### <span data-ttu-id="293da-114">Örnek 1: ada göre adlandırılmış değeri alma</span><span class="sxs-lookup"><span data-stu-id="293da-114">Example 1: Get Named Value by name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementNamedValue -Context $apimContext -Name "sql-connectionstring"
```

<span data-ttu-id="293da-115">Bu komut, adlandırılmış değer adı verilen değer ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="293da-115">This command gets the named value details given the named value name.</span></span>

## <span data-ttu-id="293da-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="293da-116">PARAMETERS</span></span>

### <span data-ttu-id="293da-117">-Context</span><span class="sxs-lookup"><span data-stu-id="293da-117">-Context</span></span>
<span data-ttu-id="293da-118">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="293da-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="293da-119">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="293da-119">This parameter is required.</span></span>

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

### <span data-ttu-id="293da-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="293da-120">-DefaultProfile</span></span>
<span data-ttu-id="293da-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="293da-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="293da-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="293da-122">-Name</span></span>
<span data-ttu-id="293da-123">Dize adını içeren adlara sahip adlandırılmış değerleri bulur.</span><span class="sxs-lookup"><span data-stu-id="293da-123">Finds named values with names containing the string Name.</span></span>
<span data-ttu-id="293da-124">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="293da-124">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="293da-125">Namedvalueıd</span><span class="sxs-lookup"><span data-stu-id="293da-125">-NamedValueId</span></span>
<span data-ttu-id="293da-126">Adlandırılmış değerin tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="293da-126">Identifier of the named value.</span></span>
<span data-ttu-id="293da-127">Belirtilmişse tanımlayıcı tarafından adlandırılmış değer bulmayı dener.</span><span class="sxs-lookup"><span data-stu-id="293da-127">If specified will try to find named value by the identifier.</span></span>
<span data-ttu-id="293da-128">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="293da-128">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNamedValueId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="293da-129">Etiketli</span><span class="sxs-lookup"><span data-stu-id="293da-129">-Tag</span></span>
<span data-ttu-id="293da-130">Etiketle ilişkilendirilmiş adlandırılmış değerleri bulur.</span><span class="sxs-lookup"><span data-stu-id="293da-130">Finds named values associated with a Tag.</span></span>
<span data-ttu-id="293da-131">Belirtilmişse bir etiketle ilişkilendirilmiş tüm özellikleri döndürür.</span><span class="sxs-lookup"><span data-stu-id="293da-131">If specified will return all properties associated with a tag.</span></span>
<span data-ttu-id="293da-132">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="293da-132">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByTag
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="293da-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="293da-133">CommonParameters</span></span>
<span data-ttu-id="293da-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="293da-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="293da-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="293da-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="293da-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="293da-136">INPUTS</span></span>

### <span data-ttu-id="293da-137">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="293da-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="293da-138">System. String</span><span class="sxs-lookup"><span data-stu-id="293da-138">System.String</span></span>

## <span data-ttu-id="293da-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="293da-139">OUTPUTS</span></span>

### <span data-ttu-id="293da-140">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementnamedvalue</span><span class="sxs-lookup"><span data-stu-id="293da-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValue</span></span>

## <span data-ttu-id="293da-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="293da-141">NOTES</span></span>

## <span data-ttu-id="293da-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="293da-142">RELATED LINKS</span></span>
