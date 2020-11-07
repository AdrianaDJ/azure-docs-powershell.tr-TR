---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A935ABAC-6C60-4AE3-9434-B9BCC1182A34
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementLogger.md
ms.openlocfilehash: 219c78dbcd39a922f98a185deb1e6ce6f0c3b652
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753585"
---
# <span data-ttu-id="f98d5-101">Get-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="f98d5-101">Get-AzApiManagementLogger</span></span>

## <span data-ttu-id="f98d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f98d5-102">SYNOPSIS</span></span>
<span data-ttu-id="f98d5-103">API yönetim günlükçüsü nesnelerini alır.</span><span class="sxs-lookup"><span data-stu-id="f98d5-103">Gets API Management Logger objects.</span></span>

## <span data-ttu-id="f98d5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f98d5-104">SYNTAX</span></span>

### <span data-ttu-id="f98d5-105">Getalllogger (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f98d5-105">GetAllLoggers (Default)</span></span>
```
Get-AzApiManagementLogger -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f98d5-106">Getbyloggerıd</span><span class="sxs-lookup"><span data-stu-id="f98d5-106">GetByLoggerId</span></span>
```
Get-AzApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f98d5-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="f98d5-107">DESCRIPTION</span></span>
<span data-ttu-id="f98d5-108">**Get-Azapsananagementgünlükçü** cmdlet 'ı BIR Azure API Yönetim **günlükçüsü** veya tüm günlük defterleri alır.</span><span class="sxs-lookup"><span data-stu-id="f98d5-108">The **Get-AzApiManagementLogger** cmdlet gets an Azure API Management **Logger** or all the loggers.</span></span>

## <span data-ttu-id="f98d5-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f98d5-109">EXAMPLES</span></span>

### <span data-ttu-id="f98d5-110">Örnek 1: tüm günlüklere ulaşın</span><span class="sxs-lookup"><span data-stu-id="f98d5-110">Example 1: Get all loggers</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementLogger -Context $apimContext
```

<span data-ttu-id="f98d5-111">Bu komut belirtilen bağlam için tüm günlüğü alır.</span><span class="sxs-lookup"><span data-stu-id="f98d5-111">This command gets all the loggers for the specified context.</span></span>

### <span data-ttu-id="f98d5-112">Örnek 2: belirli bir günlükçü alma</span><span class="sxs-lookup"><span data-stu-id="f98d5-112">Example 2: Get a specific logger</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementLogger -Context $apimContext -LoggerId "Logger123"
```

<span data-ttu-id="f98d5-113">Bu komut, KIMLIĞI Logger123 olan bir günlükçüsü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f98d5-113">This command removes a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="f98d5-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f98d5-114">PARAMETERS</span></span>

### <span data-ttu-id="f98d5-115">-Context</span><span class="sxs-lookup"><span data-stu-id="f98d5-115">-Context</span></span>
<span data-ttu-id="f98d5-116">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f98d5-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="f98d5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f98d5-117">-DefaultProfile</span></span>
<span data-ttu-id="f98d5-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f98d5-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f98d5-119">-Loggerıd</span><span class="sxs-lookup"><span data-stu-id="f98d5-119">-LoggerId</span></span>
<span data-ttu-id="f98d5-120">Alınacak belirli bir günlükçü KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="f98d5-120">Specifies the ID of the specific logger to get.</span></span>

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

### <span data-ttu-id="f98d5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f98d5-121">CommonParameters</span></span>
<span data-ttu-id="f98d5-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f98d5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f98d5-123">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="f98d5-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f98d5-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f98d5-124">INPUTS</span></span>

### <span data-ttu-id="f98d5-125">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="f98d5-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f98d5-126">System. String</span><span class="sxs-lookup"><span data-stu-id="f98d5-126">System.String</span></span>

## <span data-ttu-id="f98d5-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f98d5-127">OUTPUTS</span></span>

### <span data-ttu-id="f98d5-128">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementgünlükçü</span><span class="sxs-lookup"><span data-stu-id="f98d5-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="f98d5-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f98d5-129">NOTES</span></span>

## <span data-ttu-id="f98d5-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f98d5-130">RELATED LINKS</span></span>

[<span data-ttu-id="f98d5-131">Yeni-Azsız</span><span class="sxs-lookup"><span data-stu-id="f98d5-131">New-AzApiManagementLogger</span></span>](./New-AzApiManagementLogger.md)

[<span data-ttu-id="f98d5-132">Remove-Azapsananagementgünlükçü</span><span class="sxs-lookup"><span data-stu-id="f98d5-132">Remove-AzApiManagementLogger</span></span>](./Remove-AzApiManagementLogger.md)

[<span data-ttu-id="f98d5-133">Set-Azapsananagementgünlükçü</span><span class="sxs-lookup"><span data-stu-id="f98d5-133">Set-AzApiManagementLogger</span></span>](./Set-AzApiManagementLogger.md)


