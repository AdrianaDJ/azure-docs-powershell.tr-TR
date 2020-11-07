---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 894297BF-2771-4871-9E4C-8684364DAC4B
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementProperty.md
ms.openlocfilehash: ad6e2aebcc5a4edcf5acd3255385b0e78f317627
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751148"
---
# <span data-ttu-id="2236e-101">Get-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="2236e-101">Get-AzApiManagementProperty</span></span>

## <span data-ttu-id="2236e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2236e-102">SYNOPSIS</span></span>
<span data-ttu-id="2236e-103">Bir listeyi veya belirli bir özelliği (adlandırılmış değer) alır.</span><span class="sxs-lookup"><span data-stu-id="2236e-103">Gets a list or a particular Property (Named-Value).</span></span>

## <span data-ttu-id="2236e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2236e-104">SYNTAX</span></span>

### <span data-ttu-id="2236e-105">GetAllProperties (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2236e-105">GetAllProperties (Default)</span></span>
```
Get-AzApiManagementProperty -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2236e-106">Getbypropertyıd</span><span class="sxs-lookup"><span data-stu-id="2236e-106">GetByPropertyId</span></span>
```
Get-AzApiManagementProperty -Context <PsApiManagementContext> [-PropertyId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2236e-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="2236e-107">GetByName</span></span>
```
Get-AzApiManagementProperty -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2236e-108">GetByTag</span><span class="sxs-lookup"><span data-stu-id="2236e-108">GetByTag</span></span>
```
Get-AzApiManagementProperty -Context <PsApiManagementContext> [-Tag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2236e-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="2236e-109">DESCRIPTION</span></span>
<span data-ttu-id="2236e-110">**Get-Azapsananagementproperty** cmdlet 'i, bir liste veya belirli bir özelliği alır.</span><span class="sxs-lookup"><span data-stu-id="2236e-110">The **Get-AzApiManagementProperty** cmdlet gets a list or a particular property.</span></span>

## <span data-ttu-id="2236e-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2236e-111">EXAMPLES</span></span>

### <span data-ttu-id="2236e-112">Örnek 1: ada göre Özellik Al</span><span class="sxs-lookup"><span data-stu-id="2236e-112">Example 1: Get Property by name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementProperty -Context $apimContext -Name "sql-connectionstring"
```

## <span data-ttu-id="2236e-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2236e-113">PARAMETERS</span></span>

### <span data-ttu-id="2236e-114">-Context</span><span class="sxs-lookup"><span data-stu-id="2236e-114">-Context</span></span>
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

### <span data-ttu-id="2236e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2236e-115">-DefaultProfile</span></span>
<span data-ttu-id="2236e-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2236e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2236e-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="2236e-117">-Name</span></span>
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

### <span data-ttu-id="2236e-118">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="2236e-118">-PropertyId</span></span>
```yaml
Type: System.String
Parameter Sets: GetByPropertyId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2236e-119">Etiketli</span><span class="sxs-lookup"><span data-stu-id="2236e-119">-Tag</span></span>
<span data-ttu-id="2236e-120">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="2236e-120">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="2236e-121">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="2236e-121">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="2236e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2236e-122">CommonParameters</span></span>
<span data-ttu-id="2236e-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2236e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2236e-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2236e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2236e-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2236e-125">INPUTS</span></span>

### <span data-ttu-id="2236e-126">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="2236e-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2236e-127">System. String</span><span class="sxs-lookup"><span data-stu-id="2236e-127">System.String</span></span>

## <span data-ttu-id="2236e-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2236e-128">OUTPUTS</span></span>

### <span data-ttu-id="2236e-129">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementproperty</span><span class="sxs-lookup"><span data-stu-id="2236e-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="2236e-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2236e-130">NOTES</span></span>

## <span data-ttu-id="2236e-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2236e-131">RELATED LINKS</span></span>
