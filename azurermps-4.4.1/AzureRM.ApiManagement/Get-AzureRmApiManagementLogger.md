---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: A935ABAC-6C60-4AE3-9434-B9BCC1182A34
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementLogger.md
ms.openlocfilehash: 48033c250286c59e2cadfadc1a5b5d28f869a66c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592689"
---
# <span data-ttu-id="0742d-101">Get-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="0742d-101">Get-AzureRmApiManagementLogger</span></span>

## <span data-ttu-id="0742d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0742d-102">SYNOPSIS</span></span>
<span data-ttu-id="0742d-103">API yönetim günlükçüsü nesnelerini alır.</span><span class="sxs-lookup"><span data-stu-id="0742d-103">Gets API Management Logger objects.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0742d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0742d-104">SYNTAX</span></span>

### <span data-ttu-id="0742d-105">Tüm günlüklere ulaşın (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0742d-105">Get all loggers (Default)</span></span>
```
Get-AzureRmApiManagementLogger -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0742d-106">Günlükçü KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="0742d-106">Get by logger ID</span></span>
```
Get-AzureRmApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0742d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="0742d-107">DESCRIPTION</span></span>
<span data-ttu-id="0742d-108">**Get-Azurermapsananagementgünlükçü** cmdlet 'ı BIR Azure API Yönetim **günlükçüsü** veya tüm günlükleri alır.</span><span class="sxs-lookup"><span data-stu-id="0742d-108">The **Get-AzureRmApiManagementLogger** cmdlet gets an Azure API Management **Logger** or all the loggers.</span></span>

## <span data-ttu-id="0742d-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0742d-109">EXAMPLES</span></span>

### <span data-ttu-id="0742d-110">Örnek 1: tüm günlüklere ulaşın</span><span class="sxs-lookup"><span data-stu-id="0742d-110">Example 1: Get all loggers</span></span>
```
PS C:\>Get-AzureRmApiManagementLogger -Context $ApimContext
```

<span data-ttu-id="0742d-111">Bu komut belirtilen bağlam için tüm günlüğü alır.</span><span class="sxs-lookup"><span data-stu-id="0742d-111">This command gets all the loggers for the specified context.</span></span>

### <span data-ttu-id="0742d-112">Örnek 2: belirli bir günlükçü alma</span><span class="sxs-lookup"><span data-stu-id="0742d-112">Example 2: Get a specific logger</span></span>
```
PS C:\>Get-AzureRmApiManagementLogger -Context $ApimContext -LoggerId "Logger123"
```

<span data-ttu-id="0742d-113">Bu komut, KIMLIĞI Logger123 olan bir günlükçüsü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0742d-113">This command removes a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="0742d-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0742d-114">PARAMETERS</span></span>

### <span data-ttu-id="0742d-115">-Context</span><span class="sxs-lookup"><span data-stu-id="0742d-115">-Context</span></span>
<span data-ttu-id="0742d-116">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0742d-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="0742d-117">-Loggerıd</span><span class="sxs-lookup"><span data-stu-id="0742d-117">-LoggerId</span></span>
<span data-ttu-id="0742d-118">Alınacak belirli bir günlükçü KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="0742d-118">Specifies the ID of the specific logger to get.</span></span>

```yaml
Type: System.String
Parameter Sets: Get by logger ID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0742d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0742d-119">-DefaultProfile</span></span>
<span data-ttu-id="0742d-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0742d-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0742d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0742d-121">CommonParameters</span></span>
<span data-ttu-id="0742d-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0742d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0742d-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0742d-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0742d-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0742d-124">INPUTS</span></span>

## <span data-ttu-id="0742d-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0742d-125">OUTPUTS</span></span>

### <span data-ttu-id="0742d-126">IList<Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementgünlükçü></span><span class="sxs-lookup"><span data-stu-id="0742d-126">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger></span></span>

## <span data-ttu-id="0742d-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0742d-127">NOTES</span></span>

## <span data-ttu-id="0742d-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0742d-128">RELATED LINKS</span></span>

[<span data-ttu-id="0742d-129">Yeni-Azurermapımanagementgünlükçü</span><span class="sxs-lookup"><span data-stu-id="0742d-129">New-AzureRmApiManagementLogger</span></span>](./New-AzureRmApiManagementLogger.md)

[<span data-ttu-id="0742d-130">Remove-Azurermapımanagementgünlükçü</span><span class="sxs-lookup"><span data-stu-id="0742d-130">Remove-AzureRmApiManagementLogger</span></span>](./Remove-AzureRmApiManagementLogger.md)

[<span data-ttu-id="0742d-131">Set-Azurermapımanagementgünlükçü</span><span class="sxs-lookup"><span data-stu-id="0742d-131">Set-AzureRmApiManagementLogger</span></span>](./Set-AzureRmApiManagementLogger.md)


