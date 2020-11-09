---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: D5EB9AFA-B56C-45E2-838B-4555ED1EF8F8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOperation.md
ms.openlocfilehash: 568e3562a199a3fc247de41a30a4383bdb37adac
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324034"
---
# <span data-ttu-id="efd50-101">Get-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="efd50-101">Get-AzApiManagementOperation</span></span>

## <span data-ttu-id="efd50-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="efd50-102">SYNOPSIS</span></span>
<span data-ttu-id="efd50-103">Bir listeyi veya belirli bir API Işlemini alır.</span><span class="sxs-lookup"><span data-stu-id="efd50-103">Gets a list or a specified API Operation.</span></span>

## <span data-ttu-id="efd50-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="efd50-104">SYNTAX</span></span>

### <span data-ttu-id="efd50-105">GetAllApiOperations (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="efd50-105">GetAllApiOperations (Default)</span></span>
```
Get-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="efd50-106">GetById</span><span class="sxs-lookup"><span data-stu-id="efd50-106">GetById</span></span>
```
Get-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -OperationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="efd50-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="efd50-107">DESCRIPTION</span></span>
<span data-ttu-id="efd50-108">**Get-Azapsanana,** bir liste veya BELIRTILEN bir API işlemini alır.</span><span class="sxs-lookup"><span data-stu-id="efd50-108">The **Get-AzApiManagementOperation** gets a list or a specified API Operation.</span></span>

## <span data-ttu-id="efd50-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="efd50-109">EXAMPLES</span></span>

### <span data-ttu-id="efd50-110">Örnek 1: tüm API yönetim işlemlerini alma</span><span class="sxs-lookup"><span data-stu-id="efd50-110">Example 1: Get all API management operations</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOperation -Context $apimContext -ApiId $APIId
```

<span data-ttu-id="efd50-111">Bu komut tüm API yönetim işlemlerini alır.</span><span class="sxs-lookup"><span data-stu-id="efd50-111">This command gets all API management operations.</span></span>

### <span data-ttu-id="efd50-112">Örnek 2: işlem KIMLIĞINE göre bir API yönetim işlemi alma</span><span class="sxs-lookup"><span data-stu-id="efd50-112">Example 2: Get an API Management operation by operation ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOperation -Context $apimContext -ApiId $APIId -OperationId "Operation003"
```

<span data-ttu-id="efd50-113">Bu komut, Operation0003 adlı işlem KIMLIĞINE göre bir API yönetim işlemi alır.</span><span class="sxs-lookup"><span data-stu-id="efd50-113">This command gets an API management operation by operation ID named Operation0003.</span></span>

## <span data-ttu-id="efd50-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="efd50-114">PARAMETERS</span></span>

### <span data-ttu-id="efd50-115">-Apııd</span><span class="sxs-lookup"><span data-stu-id="efd50-115">-ApiId</span></span>
<span data-ttu-id="efd50-116">API Işleminin tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="efd50-116">Specifies the identifier of the API Operation.</span></span>

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

### <span data-ttu-id="efd50-117">-Apırevision</span><span class="sxs-lookup"><span data-stu-id="efd50-117">-ApiRevision</span></span>
<span data-ttu-id="efd50-118">API düzeltme tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="efd50-118">Identifier of API Revision.</span></span> <span data-ttu-id="efd50-119">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="efd50-119">This parameter is optional.</span></span> <span data-ttu-id="efd50-120">Belirtilmezse, işlem geçerli API düzeltmesidir.</span><span class="sxs-lookup"><span data-stu-id="efd50-120">If not specified, the operation will be retrieved from the currently active api revision.</span></span>

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

### <span data-ttu-id="efd50-121">-Context</span><span class="sxs-lookup"><span data-stu-id="efd50-121">-Context</span></span>
<span data-ttu-id="efd50-122">**Psapimanagementcontext** nesnesinin örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="efd50-122">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="efd50-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efd50-123">-DefaultProfile</span></span>
<span data-ttu-id="efd50-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="efd50-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="efd50-125">-OperationId</span><span class="sxs-lookup"><span data-stu-id="efd50-125">-OperationId</span></span>
<span data-ttu-id="efd50-126">İşlem tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="efd50-126">Specifies the operation identifier.</span></span>

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

### <span data-ttu-id="efd50-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efd50-127">CommonParameters</span></span>
<span data-ttu-id="efd50-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="efd50-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efd50-129">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="efd50-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efd50-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="efd50-130">INPUTS</span></span>

### <span data-ttu-id="efd50-131">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="efd50-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="efd50-132">System. String</span><span class="sxs-lookup"><span data-stu-id="efd50-132">System.String</span></span>

## <span data-ttu-id="efd50-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="efd50-133">OUTPUTS</span></span>

### <span data-ttu-id="efd50-134">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementoperation</span><span class="sxs-lookup"><span data-stu-id="efd50-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="efd50-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="efd50-135">NOTES</span></span>

## <span data-ttu-id="efd50-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="efd50-136">RELATED LINKS</span></span>

[<span data-ttu-id="efd50-137">Yeni-Azsız</span><span class="sxs-lookup"><span data-stu-id="efd50-137">New-AzApiManagementOperation</span></span>](./New-AzApiManagementOperation.md)

[<span data-ttu-id="efd50-138">Remove-Azapsananagementoperation</span><span class="sxs-lookup"><span data-stu-id="efd50-138">Remove-AzApiManagementOperation</span></span>](./Remove-AzApiManagementOperation.md)

[<span data-ttu-id="efd50-139">Set-Azapsananagementoperation</span><span class="sxs-lookup"><span data-stu-id="efd50-139">Set-AzApiManagementOperation</span></span>](./Set-AzApiManagementOperation.md)


