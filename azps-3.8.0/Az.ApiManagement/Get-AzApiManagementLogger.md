---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A935ABAC-6C60-4AE3-9434-B9BCC1182A34
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementLogger.md
ms.openlocfilehash: c4b7246a2b600c1ed0d9f8a01ea3fd69cd4af33d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096652"
---
# <span data-ttu-id="65892-101">Get-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="65892-101">Get-AzApiManagementLogger</span></span>

## <span data-ttu-id="65892-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65892-102">SYNOPSIS</span></span>
<span data-ttu-id="65892-103">API yönetim günlükçüsü nesnelerini alır.</span><span class="sxs-lookup"><span data-stu-id="65892-103">Gets API Management Logger objects.</span></span>

## <span data-ttu-id="65892-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="65892-104">SYNTAX</span></span>

### <span data-ttu-id="65892-105">Getalllogger (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="65892-105">GetAllLoggers (Default)</span></span>
```
Get-AzApiManagementLogger -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="65892-106">Getbyloggerıd</span><span class="sxs-lookup"><span data-stu-id="65892-106">GetByLoggerId</span></span>
```
Get-AzApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65892-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="65892-107">DESCRIPTION</span></span>
<span data-ttu-id="65892-108">**Get-Azapsananagementgünlükçü** cmdlet 'ı BIR Azure API Yönetim **günlükçüsü** veya tüm günlük defterleri alır.</span><span class="sxs-lookup"><span data-stu-id="65892-108">The **Get-AzApiManagementLogger** cmdlet gets an Azure API Management **Logger** or all the loggers.</span></span>

## <span data-ttu-id="65892-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="65892-109">EXAMPLES</span></span>

### <span data-ttu-id="65892-110">Örnek 1: tüm günlüklere ulaşın</span><span class="sxs-lookup"><span data-stu-id="65892-110">Example 1: Get all loggers</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementLogger -Context $apimContext
```

<span data-ttu-id="65892-111">Bu komut belirtilen bağlam için tüm günlüğü alır.</span><span class="sxs-lookup"><span data-stu-id="65892-111">This command gets all the loggers for the specified context.</span></span>

### <span data-ttu-id="65892-112">Örnek 2: belirli bir günlükçü alma</span><span class="sxs-lookup"><span data-stu-id="65892-112">Example 2: Get a specific logger</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementLogger -Context $apimContext -LoggerId "Logger123"
```

<span data-ttu-id="65892-113">Bu komut, KIMLIĞI Logger123 olan bir günlükçüsü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="65892-113">This command removes a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="65892-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="65892-114">PARAMETERS</span></span>

### <span data-ttu-id="65892-115">-Context</span><span class="sxs-lookup"><span data-stu-id="65892-115">-Context</span></span>
<span data-ttu-id="65892-116">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="65892-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="65892-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65892-117">-DefaultProfile</span></span>
<span data-ttu-id="65892-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="65892-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65892-119">-Loggerıd</span><span class="sxs-lookup"><span data-stu-id="65892-119">-LoggerId</span></span>
<span data-ttu-id="65892-120">Alınacak belirli bir günlükçü KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="65892-120">Specifies the ID of the specific logger to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByLoggerId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65892-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65892-121">CommonParameters</span></span>
<span data-ttu-id="65892-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="65892-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65892-123">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="65892-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65892-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="65892-124">INPUTS</span></span>

### <span data-ttu-id="65892-125">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="65892-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="65892-126">System. String</span><span class="sxs-lookup"><span data-stu-id="65892-126">System.String</span></span>

## <span data-ttu-id="65892-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="65892-127">OUTPUTS</span></span>

### <span data-ttu-id="65892-128">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementgünlükçü</span><span class="sxs-lookup"><span data-stu-id="65892-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="65892-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="65892-129">NOTES</span></span>

## <span data-ttu-id="65892-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="65892-130">RELATED LINKS</span></span>

[<span data-ttu-id="65892-131">Yeni-Azsız</span><span class="sxs-lookup"><span data-stu-id="65892-131">New-AzApiManagementLogger</span></span>](./New-AzApiManagementLogger.md)

[<span data-ttu-id="65892-132">Remove-Azapsananagementgünlükçü</span><span class="sxs-lookup"><span data-stu-id="65892-132">Remove-AzApiManagementLogger</span></span>](./Remove-AzApiManagementLogger.md)

[<span data-ttu-id="65892-133">Set-Azapsananagementgünlükçü</span><span class="sxs-lookup"><span data-stu-id="65892-133">Set-AzApiManagementLogger</span></span>](./Set-AzApiManagementLogger.md)


