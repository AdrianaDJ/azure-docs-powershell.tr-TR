---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 5B4ADD38-FA22-4C25-9B9C-FD7861883811
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementLogger.md
ms.openlocfilehash: 16a60f5f9951aaa40ac8da8584e1c2690206cdb7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594512"
---
# <span data-ttu-id="435fe-101">Set-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="435fe-101">Set-AzureRmApiManagementLogger</span></span>

## <span data-ttu-id="435fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="435fe-102">SYNOPSIS</span></span>
<span data-ttu-id="435fe-103">Bir API yönetim günlükçüsü değiştirir.</span><span class="sxs-lookup"><span data-stu-id="435fe-103">Modifies an API Management Logger.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="435fe-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="435fe-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-Name <String>]
 [-ConnectionString <String>] [-Description <String>] [-IsBuffered] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="435fe-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="435fe-105">DESCRIPTION</span></span>
<span data-ttu-id="435fe-106">**Set-Azurermapsananabir** Azure API Yönetim **günlükçüsü** ayarlarını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="435fe-106">The **Set-AzureRmApiManagementLogger** cmdlet modifies settings of an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="435fe-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="435fe-107">EXAMPLES</span></span>

### <span data-ttu-id="435fe-108">Örnek 1: günlükçü değiştirme</span><span class="sxs-lookup"><span data-stu-id="435fe-108">Example 1: Modify a logger</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementLogger -Context $apimContext -LoggerId "Logger123" -Name "ContosoSdkEventHub" -ConnectionString "Endpoint=sb://ContosoSdkEventHubs.servicebus.windows.net/;SharedAccessKeyName=SendKey;SharedAccessKey=<key>" -Description "updated SDK event hub logger" -PassThru
```

<span data-ttu-id="435fe-109">Bu komut, KIMLIĞI Logger123 olan bir günlükçüsü değiştirir.</span><span class="sxs-lookup"><span data-stu-id="435fe-109">This command modifies a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="435fe-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="435fe-110">PARAMETERS</span></span>

### <span data-ttu-id="435fe-111">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="435fe-111">-ConnectionString</span></span>
<span data-ttu-id="435fe-112">İlke haklarını içeren bir Azure etkinliği hub bağlantı dizesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="435fe-112">Specifies an Azure Event Hubs connection string that includes Send policy rights.</span></span>

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

### <span data-ttu-id="435fe-113">-Context</span><span class="sxs-lookup"><span data-stu-id="435fe-113">-Context</span></span>
<span data-ttu-id="435fe-114">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="435fe-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="435fe-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="435fe-115">-DefaultProfile</span></span>
<span data-ttu-id="435fe-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="435fe-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="435fe-117">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="435fe-117">-Description</span></span>
<span data-ttu-id="435fe-118">Bir açıklama belirtir.</span><span class="sxs-lookup"><span data-stu-id="435fe-118">Specifies a description.</span></span>

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

### <span data-ttu-id="435fe-119">-Isarabellekli</span><span class="sxs-lookup"><span data-stu-id="435fe-119">-IsBuffered</span></span>
<span data-ttu-id="435fe-120">Kayıt defterinde, yayımlamadan önce arabelleğe alınan kayıtların arabelleğe alınıp alınmayacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="435fe-120">Specifies that the records in the logger are buffered before publishing.</span></span>
<span data-ttu-id="435fe-121">Kayıtlar arabelleğe alındıklarında, her 15 saniyede bir olay hublara veya arabellek 256 KB ileti aldığında gönderilir.</span><span class="sxs-lookup"><span data-stu-id="435fe-121">When records are buffered, they are sent to Event Hubs every 15 seconds, or whenever the buffer receives 256 KB of messages.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="435fe-122">-Loggerıd</span><span class="sxs-lookup"><span data-stu-id="435fe-122">-LoggerId</span></span>
<span data-ttu-id="435fe-123">Güncelleştirilecek günlükçü KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="435fe-123">Specifies the ID of the logger to update.</span></span>

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

### <span data-ttu-id="435fe-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="435fe-124">-Name</span></span>
<span data-ttu-id="435fe-125">Azure Classic Portal 'dan bir olay hub 'ının varlık adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="435fe-125">Specifies the entity name of an event hub from Azure classic portal.</span></span>

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

### <span data-ttu-id="435fe-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="435fe-126">-PassThru</span></span>
<span data-ttu-id="435fe-127">Bu cmdlet 'in değiştirdiği  **Psapsananagementgünlükçü** değerini geri aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="435fe-127">Indicates that this cmdlet returns the  **PsApiManagementLogger** that this cmdlet modifies.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="435fe-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="435fe-128">CommonParameters</span></span>
<span data-ttu-id="435fe-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="435fe-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="435fe-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="435fe-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="435fe-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="435fe-131">INPUTS</span></span>

### <span data-ttu-id="435fe-132">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="435fe-132">None</span></span>
<span data-ttu-id="435fe-133">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="435fe-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="435fe-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="435fe-134">OUTPUTS</span></span>

### <span data-ttu-id="435fe-135">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementgünlükçü</span><span class="sxs-lookup"><span data-stu-id="435fe-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="435fe-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="435fe-136">NOTES</span></span>

## <span data-ttu-id="435fe-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="435fe-137">RELATED LINKS</span></span>

[<span data-ttu-id="435fe-138">Get-Azurermapımanagementgünlükçü</span><span class="sxs-lookup"><span data-stu-id="435fe-138">Get-AzureRmApiManagementLogger</span></span>](./Get-AzureRmApiManagementLogger.md)

[<span data-ttu-id="435fe-139">Yeni-Azurermapımanagementgünlükçü</span><span class="sxs-lookup"><span data-stu-id="435fe-139">New-AzureRmApiManagementLogger</span></span>](./New-AzureRmApiManagementLogger.md)

[<span data-ttu-id="435fe-140">Remove-Azurermapımanagementgünlükçü</span><span class="sxs-lookup"><span data-stu-id="435fe-140">Remove-AzureRmApiManagementLogger</span></span>](./Remove-AzureRmApiManagementLogger.md)


