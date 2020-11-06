---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: D5EB9AFA-B56C-45E2-838B-4555ED1EF8F8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOperation.md
ms.openlocfilehash: b2c623d46dcc2d84e2c90ae5f3d94cfb54f7224a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591255"
---
# <span data-ttu-id="94d3c-101">Get-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="94d3c-101">Get-AzureRmApiManagementOperation</span></span>

## <span data-ttu-id="94d3c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94d3c-102">SYNOPSIS</span></span>
<span data-ttu-id="94d3c-103">Bir listeyi veya belirli bir API Işlemini alır.</span><span class="sxs-lookup"><span data-stu-id="94d3c-103">Gets a list or a specified API Operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="94d3c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="94d3c-104">SYNTAX</span></span>

### <span data-ttu-id="94d3c-105">Tüm API Işlemleri (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="94d3c-105">All API Operations (Default)</span></span>
```
Get-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94d3c-106">KIMLIĞE göre bul</span><span class="sxs-lookup"><span data-stu-id="94d3c-106">Find by ID</span></span>
```
Get-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94d3c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="94d3c-107">DESCRIPTION</span></span>
<span data-ttu-id="94d3c-108">**Get-Azurermapımanatoperation** , bir listeyi veya belırlı bir API işlemini alır.</span><span class="sxs-lookup"><span data-stu-id="94d3c-108">The **Get-AzureRmApiManagementOperation** gets a list or a specified API Operation.</span></span>

## <span data-ttu-id="94d3c-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="94d3c-109">EXAMPLES</span></span>

### <span data-ttu-id="94d3c-110">Örnek 1: tüm API yönetim işlemlerini alma</span><span class="sxs-lookup"><span data-stu-id="94d3c-110">Example 1: Get all API management operations</span></span>
```
PS C:\>Get-AzureRmApiManagementOperation -Context $APImContext -ApiId $APIId
```

<span data-ttu-id="94d3c-111">Bu komut tüm API yönetim işlemlerini alır.</span><span class="sxs-lookup"><span data-stu-id="94d3c-111">This command gets all API management operations.</span></span>

### <span data-ttu-id="94d3c-112">Örnek 2: işlem KIMLIĞINE göre bir API yönetim işlemi alma</span><span class="sxs-lookup"><span data-stu-id="94d3c-112">Example 2: Get an API Management operation by operation ID</span></span>
```
PS C:\>Get-AzureRmApiManagementOperation -Context $APImContext -ApiId $APIId -OperationId "Operation003"
```

<span data-ttu-id="94d3c-113">Bu komut, Operation0003 adlı işlem KIMLIĞINE göre bir API yönetim işlemi alır.</span><span class="sxs-lookup"><span data-stu-id="94d3c-113">This command gets an API management operation by operation ID named Operation0003.</span></span>

## <span data-ttu-id="94d3c-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="94d3c-114">PARAMETERS</span></span>

### <span data-ttu-id="94d3c-115">-Apııd</span><span class="sxs-lookup"><span data-stu-id="94d3c-115">-ApiId</span></span>
<span data-ttu-id="94d3c-116">API Işleminin tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="94d3c-116">Specifies the identifier of the API Operation.</span></span>

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

### <span data-ttu-id="94d3c-117">-Context</span><span class="sxs-lookup"><span data-stu-id="94d3c-117">-Context</span></span>
<span data-ttu-id="94d3c-118">**Psapimanagementcontext** nesnesinin örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="94d3c-118">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="94d3c-119">-OperationId</span><span class="sxs-lookup"><span data-stu-id="94d3c-119">-OperationId</span></span>
<span data-ttu-id="94d3c-120">İşlem tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="94d3c-120">Specifies the operation identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Find by ID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94d3c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94d3c-121">-DefaultProfile</span></span>
<span data-ttu-id="94d3c-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="94d3c-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94d3c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94d3c-123">CommonParameters</span></span>
<span data-ttu-id="94d3c-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="94d3c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94d3c-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94d3c-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94d3c-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="94d3c-126">INPUTS</span></span>

## <span data-ttu-id="94d3c-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="94d3c-127">OUTPUTS</span></span>

### <span data-ttu-id="94d3c-128">IList<Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementoperation></span><span class="sxs-lookup"><span data-stu-id="94d3c-128">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation></span></span>

## <span data-ttu-id="94d3c-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="94d3c-129">NOTES</span></span>

## <span data-ttu-id="94d3c-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="94d3c-130">RELATED LINKS</span></span>

[<span data-ttu-id="94d3c-131">Yeni-Azurermapsananaks</span><span class="sxs-lookup"><span data-stu-id="94d3c-131">New-AzureRmApiManagementOperation</span></span>](./New-AzureRmApiManagementOperation.md)

[<span data-ttu-id="94d3c-132">Remove-Azurermapımanagementoperation</span><span class="sxs-lookup"><span data-stu-id="94d3c-132">Remove-AzureRmApiManagementOperation</span></span>](./Remove-AzureRmApiManagementOperation.md)

[<span data-ttu-id="94d3c-133">Set-Azurermapımanagementoperation</span><span class="sxs-lookup"><span data-stu-id="94d3c-133">Set-AzureRmApiManagementOperation</span></span>](./Set-AzureRmApiManagementOperation.md)


