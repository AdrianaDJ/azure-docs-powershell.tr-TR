---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: D5EB9AFA-B56C-45E2-838B-4555ED1EF8F8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOperation.md
ms.openlocfilehash: 1b1547485a4758764cf02eaca4fd7bc26d4ef990
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592988"
---
# <span data-ttu-id="0629e-101">Get-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="0629e-101">Get-AzureRmApiManagementOperation</span></span>

## <span data-ttu-id="0629e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0629e-102">SYNOPSIS</span></span>
<span data-ttu-id="0629e-103">Bir listeyi veya belirli bir API Işlemini alır.</span><span class="sxs-lookup"><span data-stu-id="0629e-103">Gets a list or a specified API Operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0629e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0629e-104">SYNTAX</span></span>

### <span data-ttu-id="0629e-105">GetAllApiOperations (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0629e-105">GetAllApiOperations (Default)</span></span>
```
Get-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0629e-106">GetById</span><span class="sxs-lookup"><span data-stu-id="0629e-106">GetById</span></span>
```
Get-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0629e-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="0629e-107">DESCRIPTION</span></span>
<span data-ttu-id="0629e-108">**Get-Azurermapımanatoperation** , bir listeyi veya belırlı bir API işlemini alır.</span><span class="sxs-lookup"><span data-stu-id="0629e-108">The **Get-AzureRmApiManagementOperation** gets a list or a specified API Operation.</span></span>

## <span data-ttu-id="0629e-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0629e-109">EXAMPLES</span></span>

### <span data-ttu-id="0629e-110">Örnek 1: tüm API yönetim işlemlerini alma</span><span class="sxs-lookup"><span data-stu-id="0629e-110">Example 1: Get all API management operations</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementOperation -Context $apimContext -ApiId $APIId
```

<span data-ttu-id="0629e-111">Bu komut tüm API yönetim işlemlerini alır.</span><span class="sxs-lookup"><span data-stu-id="0629e-111">This command gets all API management operations.</span></span>

### <span data-ttu-id="0629e-112">Örnek 2: işlem KIMLIĞINE göre bir API yönetim işlemi alma</span><span class="sxs-lookup"><span data-stu-id="0629e-112">Example 2: Get an API Management operation by operation ID</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementOperation -Context $apimContext -ApiId $APIId -OperationId "Operation003"
```

<span data-ttu-id="0629e-113">Bu komut, Operation0003 adlı işlem KIMLIĞINE göre bir API yönetim işlemi alır.</span><span class="sxs-lookup"><span data-stu-id="0629e-113">This command gets an API management operation by operation ID named Operation0003.</span></span>

## <span data-ttu-id="0629e-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0629e-114">PARAMETERS</span></span>

### <span data-ttu-id="0629e-115">-Apııd</span><span class="sxs-lookup"><span data-stu-id="0629e-115">-ApiId</span></span>
<span data-ttu-id="0629e-116">API Işleminin tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0629e-116">Specifies the identifier of the API Operation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0629e-117">-Context</span><span class="sxs-lookup"><span data-stu-id="0629e-117">-Context</span></span>
<span data-ttu-id="0629e-118">**Psapimanagementcontext** nesnesinin örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0629e-118">Specifies the instance of the **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0629e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0629e-119">-DefaultProfile</span></span>
<span data-ttu-id="0629e-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0629e-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0629e-121">-OperationId</span><span class="sxs-lookup"><span data-stu-id="0629e-121">-OperationId</span></span>
<span data-ttu-id="0629e-122">İşlem tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0629e-122">Specifies the operation identifier.</span></span>

```yaml
Type: String
Parameter Sets: GetById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0629e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0629e-123">CommonParameters</span></span>
<span data-ttu-id="0629e-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0629e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0629e-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0629e-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0629e-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0629e-126">INPUTS</span></span>

### <span data-ttu-id="0629e-127">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="0629e-127">None</span></span>
<span data-ttu-id="0629e-128">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="0629e-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0629e-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0629e-129">OUTPUTS</span></span>

### <span data-ttu-id="0629e-130">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementoperation</span><span class="sxs-lookup"><span data-stu-id="0629e-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>
<span data-ttu-id="0629e-131">API Yönetimi hizmetindeki API Işleminin ayrıntıları.</span><span class="sxs-lookup"><span data-stu-id="0629e-131">The details of the API Operation in Api Management service.</span></span>

### <span data-ttu-id="0629e-132">IList<Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementoperation></span><span class="sxs-lookup"><span data-stu-id="0629e-132">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation></span></span>
<span data-ttu-id="0629e-133">API Yönetimi hizmetindeki API Işlemi listesi.</span><span class="sxs-lookup"><span data-stu-id="0629e-133">The list of API Operation in Api Management service.</span></span>

## <span data-ttu-id="0629e-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0629e-134">NOTES</span></span>

## <span data-ttu-id="0629e-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0629e-135">RELATED LINKS</span></span>

[<span data-ttu-id="0629e-136">Yeni-Azurermapsananaks</span><span class="sxs-lookup"><span data-stu-id="0629e-136">New-AzureRmApiManagementOperation</span></span>](./New-AzureRmApiManagementOperation.md)

[<span data-ttu-id="0629e-137">Remove-Azurermapımanagementoperation</span><span class="sxs-lookup"><span data-stu-id="0629e-137">Remove-AzureRmApiManagementOperation</span></span>](./Remove-AzureRmApiManagementOperation.md)

[<span data-ttu-id="0629e-138">Set-Azurermapımanagementoperation</span><span class="sxs-lookup"><span data-stu-id="0629e-138">Set-AzureRmApiManagementOperation</span></span>](./Set-AzureRmApiManagementOperation.md)


