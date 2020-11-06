---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: A935ABAC-6C60-4AE3-9434-B9BCC1182A34
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementLogger.md
ms.openlocfilehash: bcfcd052d2278fa39bc310a5c1927457a1b0fcd3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592514"
---
# <span data-ttu-id="88dc4-101">Get-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="88dc4-101">Get-AzureRmApiManagementLogger</span></span>

## <span data-ttu-id="88dc4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88dc4-102">SYNOPSIS</span></span>
<span data-ttu-id="88dc4-103">API yönetim günlükçüsü nesnelerini alır.</span><span class="sxs-lookup"><span data-stu-id="88dc4-103">Gets API Management Logger objects.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88dc4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="88dc4-104">SYNTAX</span></span>

### <span data-ttu-id="88dc4-105">Getalllogger (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="88dc4-105">GetAllLoggers (Default)</span></span>
```
Get-AzureRmApiManagementLogger -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="88dc4-106">Getbyloggerıd</span><span class="sxs-lookup"><span data-stu-id="88dc4-106">GetByLoggerId</span></span>
```
Get-AzureRmApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88dc4-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="88dc4-107">DESCRIPTION</span></span>
<span data-ttu-id="88dc4-108">**Get-Azurermapsananagementgünlükçü** cmdlet 'ı BIR Azure API Yönetim **günlükçüsü** veya tüm günlükleri alır.</span><span class="sxs-lookup"><span data-stu-id="88dc4-108">The **Get-AzureRmApiManagementLogger** cmdlet gets an Azure API Management **Logger** or all the loggers.</span></span>

## <span data-ttu-id="88dc4-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="88dc4-109">EXAMPLES</span></span>

### <span data-ttu-id="88dc4-110">Örnek 1: tüm günlüklere ulaşın</span><span class="sxs-lookup"><span data-stu-id="88dc4-110">Example 1: Get all loggers</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementLogger -Context $apimContext
```

<span data-ttu-id="88dc4-111">Bu komut belirtilen bağlam için tüm günlüğü alır.</span><span class="sxs-lookup"><span data-stu-id="88dc4-111">This command gets all the loggers for the specified context.</span></span>

### <span data-ttu-id="88dc4-112">Örnek 2: belirli bir günlükçü alma</span><span class="sxs-lookup"><span data-stu-id="88dc4-112">Example 2: Get a specific logger</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementLogger -Context $apimContext -LoggerId "Logger123"
```

<span data-ttu-id="88dc4-113">Bu komut, KIMLIĞI Logger123 olan bir günlükçüsü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="88dc4-113">This command removes a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="88dc4-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="88dc4-114">PARAMETERS</span></span>

### <span data-ttu-id="88dc4-115">-Context</span><span class="sxs-lookup"><span data-stu-id="88dc4-115">-Context</span></span>
<span data-ttu-id="88dc4-116">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="88dc4-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="88dc4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88dc4-117">-DefaultProfile</span></span>
<span data-ttu-id="88dc4-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="88dc4-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="88dc4-119">-Loggerıd</span><span class="sxs-lookup"><span data-stu-id="88dc4-119">-LoggerId</span></span>
<span data-ttu-id="88dc4-120">Alınacak belirli bir günlükçü KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="88dc4-120">Specifies the ID of the specific logger to get.</span></span>

```yaml
Type: String
Parameter Sets: GetByLoggerId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88dc4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88dc4-121">CommonParameters</span></span>
<span data-ttu-id="88dc4-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="88dc4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88dc4-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88dc4-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88dc4-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="88dc4-124">INPUTS</span></span>

### <span data-ttu-id="88dc4-125">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="88dc4-125">None</span></span>
<span data-ttu-id="88dc4-126">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="88dc4-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="88dc4-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="88dc4-127">OUTPUTS</span></span>

### <span data-ttu-id="88dc4-128">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementgünlükçü</span><span class="sxs-lookup"><span data-stu-id="88dc4-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>
<span data-ttu-id="88dc4-129">API Yönetim hizmetinde yapılandırılan günlükçü ayrıntısı.</span><span class="sxs-lookup"><span data-stu-id="88dc4-129">The detail of the Logger configured in API Management service.</span></span>

### <span data-ttu-id="88dc4-130">IList<Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementgünlükçü></span><span class="sxs-lookup"><span data-stu-id="88dc4-130">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger></span></span>
<span data-ttu-id="88dc4-131">API Yönetim hizmetinde yapılandırılmış günlük cihazları listesi.</span><span class="sxs-lookup"><span data-stu-id="88dc4-131">The list of Loggers configured in API Management service.</span></span>

## <span data-ttu-id="88dc4-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="88dc4-132">NOTES</span></span>

## <span data-ttu-id="88dc4-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="88dc4-133">RELATED LINKS</span></span>

[<span data-ttu-id="88dc4-134">Yeni-Azurermapımanagementgünlükçü</span><span class="sxs-lookup"><span data-stu-id="88dc4-134">New-AzureRmApiManagementLogger</span></span>](./New-AzureRmApiManagementLogger.md)

[<span data-ttu-id="88dc4-135">Remove-Azurermapımanagementgünlükçü</span><span class="sxs-lookup"><span data-stu-id="88dc4-135">Remove-AzureRmApiManagementLogger</span></span>](./Remove-AzureRmApiManagementLogger.md)

[<span data-ttu-id="88dc4-136">Set-Azurermapımanagementgünlükçü</span><span class="sxs-lookup"><span data-stu-id="88dc4-136">Set-AzureRmApiManagementLogger</span></span>](./Set-AzureRmApiManagementLogger.md)


