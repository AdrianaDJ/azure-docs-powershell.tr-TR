---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 17D53F56-6E3B-491E-8776-5EBE109FBE3C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementLogger.md
ms.openlocfilehash: 2929cbd89328d971b47b748d4aa042ade13c1af9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589906"
---
# <span data-ttu-id="7da55-101">New-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="7da55-101">New-AzureRmApiManagementLogger</span></span>

## <span data-ttu-id="7da55-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7da55-102">SYNOPSIS</span></span>
<span data-ttu-id="7da55-103">Bir API yönetim günlükçüsü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7da55-103">Creates an API Management Logger.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7da55-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7da55-104">SYNTAX</span></span>

```
New-AzureRmApiManagementLogger -Context <PsApiManagementContext> [-LoggerId <String>] -Name <String>
 -ConnectionString <String> [-Description <String>] [-IsBuffered <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7da55-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7da55-105">DESCRIPTION</span></span>
<span data-ttu-id="7da55-106">**Yeni-Azurermapsananagementgünlükçü** cmdlet 'ı BIR Azure API Yönetim **günlükçüsü** oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7da55-106">The **New-AzureRmApiManagementLogger** cmdlet creates an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="7da55-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7da55-107">EXAMPLES</span></span>

### <span data-ttu-id="7da55-108">Örnek 1: günlükçü oluşturma</span><span class="sxs-lookup"><span data-stu-id="7da55-108">Example 1: Create a logger</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementLogger -Context $apimContext -LoggerId "Logger123" -Name "ContosoSdkEventHub" -ConnectionString "Endpoint=sb://ContosoSdkEventHubs.servicebus.windows.net/;SharedAccessKeyName=SendKey;SharedAccessKey=<key>" -Description "SDK event hub logger"
```

<span data-ttu-id="7da55-109">Bu komut, belirtilen bağlantı dizesini kullanarak ContosoSdkEventHub adlı bir günlükçü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7da55-109">This command creates a logger named ContosoSdkEventHub by using the specified connection string.</span></span>

## <span data-ttu-id="7da55-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7da55-110">PARAMETERS</span></span>

### <span data-ttu-id="7da55-111">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="7da55-111">-ConnectionString</span></span>
<span data-ttu-id="7da55-112">Aşağıdakiler ile başlayan bir Azure Olay Hub bağlantı dizesi belirtir:</span><span class="sxs-lookup"><span data-stu-id="7da55-112">Specifies an Azure Event Hubs connection string that starts with the following:</span></span> 

`Endpoint=endpoint and key from Azure classic portal`

<span data-ttu-id="7da55-113">Bağlantı dizesindeki gönderme haklarını içeren anahtar yapılandırılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="7da55-113">The Key with Send Rights in the connection string must be configured.</span></span>

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

### <span data-ttu-id="7da55-114">-Context</span><span class="sxs-lookup"><span data-stu-id="7da55-114">-Context</span></span>
<span data-ttu-id="7da55-115">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7da55-115">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="7da55-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7da55-116">-DefaultProfile</span></span>
<span data-ttu-id="7da55-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7da55-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="7da55-118">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="7da55-118">-Description</span></span>
<span data-ttu-id="7da55-119">Bir açıklama belirtir.</span><span class="sxs-lookup"><span data-stu-id="7da55-119">Specifies a description.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7da55-120">-Isarabellekli</span><span class="sxs-lookup"><span data-stu-id="7da55-120">-IsBuffered</span></span>
<span data-ttu-id="7da55-121">Kayıt defterinde, yayımlamadan önce arabelleğe alınıp alınmadığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7da55-121">Specifies whether the records in the logger are buffered before publishing.</span></span>
<span data-ttu-id="7da55-122">Varsayılan değer $True.</span><span class="sxs-lookup"><span data-stu-id="7da55-122">The default value is $True.</span></span>
<span data-ttu-id="7da55-123">Kayıtlar arabelleğe alındıklarında, her 15 saniyede bir olay hublara veya arabellek 256 KB ileti aldığında gönderilir.</span><span class="sxs-lookup"><span data-stu-id="7da55-123">When records are buffered, they are sent to Event Hubs every 15 seconds, or whenever the buffer receives 256 KB of messages.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7da55-124">-Loggerıd</span><span class="sxs-lookup"><span data-stu-id="7da55-124">-LoggerId</span></span>
<span data-ttu-id="7da55-125">Günlükçü için bir KIMLIK belirtir.</span><span class="sxs-lookup"><span data-stu-id="7da55-125">Specifies an ID for the logger.</span></span>
<span data-ttu-id="7da55-126">KIMLIK belirtmezseniz, bu cmdlet bir tane oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7da55-126">If you do not specify an ID, this cmdlet generates one.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7da55-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="7da55-127">-Name</span></span>
<span data-ttu-id="7da55-128">Azure Classic Portal 'dan bir olay hub 'ının varlık adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7da55-128">Specifies the entity name of an event hub from Azure classic portal.</span></span>

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

### <span data-ttu-id="7da55-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7da55-129">CommonParameters</span></span>
<span data-ttu-id="7da55-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7da55-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7da55-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7da55-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7da55-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7da55-132">INPUTS</span></span>

### <span data-ttu-id="7da55-133">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="7da55-133">None</span></span>
<span data-ttu-id="7da55-134">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="7da55-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7da55-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7da55-135">OUTPUTS</span></span>

### <span data-ttu-id="7da55-136">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementgünlükçü</span><span class="sxs-lookup"><span data-stu-id="7da55-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="7da55-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7da55-137">NOTES</span></span>

## <span data-ttu-id="7da55-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7da55-138">RELATED LINKS</span></span>

[<span data-ttu-id="7da55-139">Get-Azurermapımanagementgünlükçü</span><span class="sxs-lookup"><span data-stu-id="7da55-139">Get-AzureRmApiManagementLogger</span></span>](./Get-AzureRmApiManagementLogger.md)

[<span data-ttu-id="7da55-140">Remove-Azurermapımanagementgünlükçü</span><span class="sxs-lookup"><span data-stu-id="7da55-140">Remove-AzureRmApiManagementLogger</span></span>](./Remove-AzureRmApiManagementLogger.md)

[<span data-ttu-id="7da55-141">Set-Azurermapımanagementgünlükçü</span><span class="sxs-lookup"><span data-stu-id="7da55-141">Set-AzureRmApiManagementLogger</span></span>](./Set-AzureRmApiManagementLogger.md)


