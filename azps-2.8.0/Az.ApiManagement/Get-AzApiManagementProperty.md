---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 894297BF-2771-4871-9E4C-8684364DAC4B
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementProperty.md
ms.openlocfilehash: 2c8fc24d252fce12e7adf9ee824db0e1b2c8b206
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753576"
---
# <span data-ttu-id="9bf63-101">Get-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="9bf63-101">Get-AzApiManagementProperty</span></span>

## <span data-ttu-id="9bf63-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9bf63-102">SYNOPSIS</span></span>
<span data-ttu-id="9bf63-103">Bir listeyi veya belirli bir özelliği (adlandırılmış değer) alır.</span><span class="sxs-lookup"><span data-stu-id="9bf63-103">Gets a list or a particular Property (Named-Value).</span></span>

## <span data-ttu-id="9bf63-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9bf63-104">SYNTAX</span></span>

### <span data-ttu-id="9bf63-105">GetAllProperties (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9bf63-105">GetAllProperties (Default)</span></span>
```
Get-AzApiManagementProperty -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9bf63-106">Getbypropertyıd</span><span class="sxs-lookup"><span data-stu-id="9bf63-106">GetByPropertyId</span></span>
```
Get-AzApiManagementProperty -Context <PsApiManagementContext> [-PropertyId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9bf63-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="9bf63-107">GetByName</span></span>
```
Get-AzApiManagementProperty -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9bf63-108">GetByTag</span><span class="sxs-lookup"><span data-stu-id="9bf63-108">GetByTag</span></span>
```
Get-AzApiManagementProperty -Context <PsApiManagementContext> [-Tag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9bf63-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="9bf63-109">DESCRIPTION</span></span>
<span data-ttu-id="9bf63-110">**Get-Azapsananagementproperty** cmdlet 'i, bir liste veya belirli bir özelliği alır.</span><span class="sxs-lookup"><span data-stu-id="9bf63-110">The **Get-AzApiManagementProperty** cmdlet gets a list or a particular property.</span></span>

## <span data-ttu-id="9bf63-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9bf63-111">EXAMPLES</span></span>

### <span data-ttu-id="9bf63-112">Örnek 1: ada göre Özellik Al</span><span class="sxs-lookup"><span data-stu-id="9bf63-112">Example 1: Get Property by name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementProperty -Context $apimContext -Name "sql-connectionstring"
```

## <span data-ttu-id="9bf63-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9bf63-113">PARAMETERS</span></span>

### <span data-ttu-id="9bf63-114">-Context</span><span class="sxs-lookup"><span data-stu-id="9bf63-114">-Context</span></span>
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

### <span data-ttu-id="9bf63-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bf63-115">-DefaultProfile</span></span>
<span data-ttu-id="9bf63-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9bf63-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9bf63-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="9bf63-117">-Name</span></span>
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

### <span data-ttu-id="9bf63-118">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="9bf63-118">-PropertyId</span></span>
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

### <span data-ttu-id="9bf63-119">Etiketli</span><span class="sxs-lookup"><span data-stu-id="9bf63-119">-Tag</span></span>
<span data-ttu-id="9bf63-120">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="9bf63-120">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="9bf63-121">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="9bf63-121">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="9bf63-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bf63-122">CommonParameters</span></span>
<span data-ttu-id="9bf63-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9bf63-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bf63-124">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="9bf63-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bf63-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9bf63-125">INPUTS</span></span>

### <span data-ttu-id="9bf63-126">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="9bf63-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9bf63-127">System. String</span><span class="sxs-lookup"><span data-stu-id="9bf63-127">System.String</span></span>

## <span data-ttu-id="9bf63-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9bf63-128">OUTPUTS</span></span>

### <span data-ttu-id="9bf63-129">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementproperty</span><span class="sxs-lookup"><span data-stu-id="9bf63-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="9bf63-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9bf63-130">NOTES</span></span>

## <span data-ttu-id="9bf63-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9bf63-131">RELATED LINKS</span></span>
