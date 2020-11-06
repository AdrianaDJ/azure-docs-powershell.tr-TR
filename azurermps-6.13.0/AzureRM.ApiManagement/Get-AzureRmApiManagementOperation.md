---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: D5EB9AFA-B56C-45E2-838B-4555ED1EF8F8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOperation.md
ms.openlocfilehash: 469d10303f286a0feca162e628a1564826b850d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573101"
---
# <span data-ttu-id="f46b9-101">Get-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="f46b9-101">Get-AzureRmApiManagementOperation</span></span>

## <span data-ttu-id="f46b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f46b9-102">SYNOPSIS</span></span>
<span data-ttu-id="f46b9-103">Bir listeyi veya belirli bir API Işlemini alır.</span><span class="sxs-lookup"><span data-stu-id="f46b9-103">Gets a list or a specified API Operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f46b9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f46b9-104">SYNTAX</span></span>

### <span data-ttu-id="f46b9-105">GetAllApiOperations (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f46b9-105">GetAllApiOperations (Default)</span></span>
```
Get-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f46b9-106">GetById</span><span class="sxs-lookup"><span data-stu-id="f46b9-106">GetById</span></span>
```
Get-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -OperationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f46b9-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="f46b9-107">DESCRIPTION</span></span>
<span data-ttu-id="f46b9-108">**Get-Azurermapımanatoperation** , bir listeyi veya belırlı bir API işlemini alır.</span><span class="sxs-lookup"><span data-stu-id="f46b9-108">The **Get-AzureRmApiManagementOperation** gets a list or a specified API Operation.</span></span>

## <span data-ttu-id="f46b9-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f46b9-109">EXAMPLES</span></span>

### <span data-ttu-id="f46b9-110">Örnek 1: tüm API yönetim işlemlerini alma</span><span class="sxs-lookup"><span data-stu-id="f46b9-110">Example 1: Get all API management operations</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementOperation -Context $apimContext -ApiId $APIId
```

<span data-ttu-id="f46b9-111">Bu komut tüm API yönetim işlemlerini alır.</span><span class="sxs-lookup"><span data-stu-id="f46b9-111">This command gets all API management operations.</span></span>

### <span data-ttu-id="f46b9-112">Örnek 2: işlem KIMLIĞINE göre bir API yönetim işlemi alma</span><span class="sxs-lookup"><span data-stu-id="f46b9-112">Example 2: Get an API Management operation by operation ID</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementOperation -Context $apimContext -ApiId $APIId -OperationId "Operation003"
```

<span data-ttu-id="f46b9-113">Bu komut, Operation0003 adlı işlem KIMLIĞINE göre bir API yönetim işlemi alır.</span><span class="sxs-lookup"><span data-stu-id="f46b9-113">This command gets an API management operation by operation ID named Operation0003.</span></span>

## <span data-ttu-id="f46b9-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f46b9-114">PARAMETERS</span></span>

### <span data-ttu-id="f46b9-115">-Apııd</span><span class="sxs-lookup"><span data-stu-id="f46b9-115">-ApiId</span></span>
<span data-ttu-id="f46b9-116">API Işleminin tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f46b9-116">Specifies the identifier of the API Operation.</span></span>

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

### <span data-ttu-id="f46b9-117">-Apırevision</span><span class="sxs-lookup"><span data-stu-id="f46b9-117">-ApiRevision</span></span>
<span data-ttu-id="f46b9-118">API düzeltme tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="f46b9-118">Identifier of API Revision.</span></span> <span data-ttu-id="f46b9-119">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="f46b9-119">This parameter is optional.</span></span> <span data-ttu-id="f46b9-120">Belirtilmezse, işlem geçerli API düzeltmesidir.</span><span class="sxs-lookup"><span data-stu-id="f46b9-120">If not specified, the operation will be retrieved from the currently active api revision.</span></span>

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

### <span data-ttu-id="f46b9-121">-Context</span><span class="sxs-lookup"><span data-stu-id="f46b9-121">-Context</span></span>
<span data-ttu-id="f46b9-122">**Psapimanagementcontext** nesnesinin örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f46b9-122">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="f46b9-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f46b9-123">-DefaultProfile</span></span>
<span data-ttu-id="f46b9-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f46b9-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f46b9-125">-OperationId</span><span class="sxs-lookup"><span data-stu-id="f46b9-125">-OperationId</span></span>
<span data-ttu-id="f46b9-126">İşlem tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f46b9-126">Specifies the operation identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f46b9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f46b9-127">CommonParameters</span></span>
<span data-ttu-id="f46b9-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f46b9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f46b9-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f46b9-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f46b9-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f46b9-130">INPUTS</span></span>

### <span data-ttu-id="f46b9-131">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="f46b9-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f46b9-132">System. String</span><span class="sxs-lookup"><span data-stu-id="f46b9-132">System.String</span></span>

## <span data-ttu-id="f46b9-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f46b9-133">OUTPUTS</span></span>

### <span data-ttu-id="f46b9-134">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementoperation</span><span class="sxs-lookup"><span data-stu-id="f46b9-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="f46b9-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f46b9-135">NOTES</span></span>

## <span data-ttu-id="f46b9-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f46b9-136">RELATED LINKS</span></span>

[<span data-ttu-id="f46b9-137">Yeni-Azurermapsananaks</span><span class="sxs-lookup"><span data-stu-id="f46b9-137">New-AzureRmApiManagementOperation</span></span>](./New-AzureRmApiManagementOperation.md)

[<span data-ttu-id="f46b9-138">Remove-Azurermapımanagementoperation</span><span class="sxs-lookup"><span data-stu-id="f46b9-138">Remove-AzureRmApiManagementOperation</span></span>](./Remove-AzureRmApiManagementOperation.md)

[<span data-ttu-id="f46b9-139">Set-Azurermapımanagementoperation</span><span class="sxs-lookup"><span data-stu-id="f46b9-139">Set-AzureRmApiManagementOperation</span></span>](./Set-AzureRmApiManagementOperation.md)


