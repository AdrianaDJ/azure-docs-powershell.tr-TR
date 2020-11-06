---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5B4ADD38-FA22-4C25-9B9C-FD7861883811
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementLogger.md
ms.openlocfilehash: 7a037b107f3d72a000c2f69c8de507a4f414e283
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589611"
---
# <span data-ttu-id="6d936-101">Set-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="6d936-101">Set-AzureRmApiManagementLogger</span></span>

## <span data-ttu-id="6d936-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d936-102">SYNOPSIS</span></span>
<span data-ttu-id="6d936-103">Bir API yönetim günlükçüsü değiştirir.</span><span class="sxs-lookup"><span data-stu-id="6d936-103">Modifies an API Management Logger.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6d936-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6d936-104">SYNTAX</span></span>

### <span data-ttu-id="6d936-105">EventHubLoggerSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6d936-105">EventHubLoggerSet (Default)</span></span>
```
Set-AzureRmApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-Name <String>]
 [-ConnectionString <String>] [-Description <String>] [-IsBuffered] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6d936-106">Applicationınsightsloggerset</span><span class="sxs-lookup"><span data-stu-id="6d936-106">ApplicationInsightsLoggerSet</span></span>
```
Set-AzureRmApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String>
 [-InstrumentationKey <String>] [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6d936-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="6d936-107">DESCRIPTION</span></span>
<span data-ttu-id="6d936-108">**Set-Azurermapsananabir** Azure API Yönetim **günlükçüsü** ayarlarını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="6d936-108">The **Set-AzureRmApiManagementLogger** cmdlet modifies settings of an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="6d936-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6d936-109">EXAMPLES</span></span>

### <span data-ttu-id="6d936-110">Örnek 1: EventHub günlükçüsü değiştirme</span><span class="sxs-lookup"><span data-stu-id="6d936-110">Example 1: Modify EventHub logger</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementLogger -Context $apimContext -LoggerId "Logger123" -Name "ContosoSdkEventHub" -ConnectionString "Endpoint=sb://ContosoSdkEventHubs.servicebus.windows.net/;SharedAccessKeyName=SendKey;SharedAccessKey=<key>" -Description "updated SDK event hub logger" -PassThru
```

<span data-ttu-id="6d936-111">Bu komut, KIMLIĞI Logger123 olan bir günlükçüsü değiştirir.</span><span class="sxs-lookup"><span data-stu-id="6d936-111">This command modifies a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="6d936-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6d936-112">PARAMETERS</span></span>

### <span data-ttu-id="6d936-113">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="6d936-113">-ConnectionString</span></span>
<span data-ttu-id="6d936-114">İlke haklarını içeren bir Azure etkinliği hub bağlantı dizesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d936-114">Specifies an Azure Event Hubs connection string that includes Send policy rights.</span></span>

```yaml
Type: System.String
Parameter Sets: EventHubLoggerSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d936-115">-Context</span><span class="sxs-lookup"><span data-stu-id="6d936-115">-Context</span></span>
<span data-ttu-id="6d936-116">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d936-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="6d936-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d936-117">-DefaultProfile</span></span>
<span data-ttu-id="6d936-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6d936-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6d936-119">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="6d936-119">-Description</span></span>
<span data-ttu-id="6d936-120">Bir açıklama belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d936-120">Specifies a description.</span></span>

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

### <span data-ttu-id="6d936-121">-Enstrüentationkey</span><span class="sxs-lookup"><span data-stu-id="6d936-121">-InstrumentationKey</span></span>
<span data-ttu-id="6d936-122">Application Insights 'ın alt yapısı.</span><span class="sxs-lookup"><span data-stu-id="6d936-122">Instrumentation Key of the application Insights.</span></span> <span data-ttu-id="6d936-123">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="6d936-123">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationInsightsLoggerSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d936-124">-Isarabellekli</span><span class="sxs-lookup"><span data-stu-id="6d936-124">-IsBuffered</span></span>
<span data-ttu-id="6d936-125">Kayıt defterinde, yayımlamadan önce arabelleğe alınan kayıtların arabelleğe alınıp alınmayacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d936-125">Specifies that the records in the logger are buffered before publishing.</span></span>
<span data-ttu-id="6d936-126">Kayıtlar arabelleğe alındıklarında, her 15 saniyede bir olay hublara veya arabellek 256 KB ileti aldığında gönderilir.</span><span class="sxs-lookup"><span data-stu-id="6d936-126">When records are buffered, they are sent to Event Hubs every 15 seconds, or whenever the buffer receives 256 KB of messages.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EventHubLoggerSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d936-127">-Loggerıd</span><span class="sxs-lookup"><span data-stu-id="6d936-127">-LoggerId</span></span>
<span data-ttu-id="6d936-128">Güncelleştirilecek günlükçü KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d936-128">Specifies the ID of the logger to update.</span></span>

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

### <span data-ttu-id="6d936-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="6d936-129">-Name</span></span>
<span data-ttu-id="6d936-130">Azure Classic Portal 'dan bir olay hub 'ının varlık adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d936-130">Specifies the entity name of an event hub from Azure classic portal.</span></span>

```yaml
Type: System.String
Parameter Sets: EventHubLoggerSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d936-131">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="6d936-131">-PassThru</span></span>
<span data-ttu-id="6d936-132">Bu cmdlet 'in değiştirdiği  **Psapsananagementgünlükçü** değerini geri aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6d936-132">Indicates that this cmdlet returns the  **PsApiManagementLogger** that this cmdlet modifies.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d936-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d936-133">CommonParameters</span></span>
<span data-ttu-id="6d936-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6d936-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d936-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d936-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d936-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6d936-136">INPUTS</span></span>

### <span data-ttu-id="6d936-137">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="6d936-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="6d936-138">System. String</span><span class="sxs-lookup"><span data-stu-id="6d936-138">System.String</span></span>

### <span data-ttu-id="6d936-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6d936-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6d936-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6d936-140">OUTPUTS</span></span>

### <span data-ttu-id="6d936-141">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementgünlükçü</span><span class="sxs-lookup"><span data-stu-id="6d936-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="6d936-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6d936-142">NOTES</span></span>

## <span data-ttu-id="6d936-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6d936-143">RELATED LINKS</span></span>

[<span data-ttu-id="6d936-144">Get-Azurermapımanagementgünlükçü</span><span class="sxs-lookup"><span data-stu-id="6d936-144">Get-AzureRmApiManagementLogger</span></span>](./Get-AzureRmApiManagementLogger.md)

[<span data-ttu-id="6d936-145">Yeni-Azurermapımanagementgünlükçü</span><span class="sxs-lookup"><span data-stu-id="6d936-145">New-AzureRmApiManagementLogger</span></span>](./New-AzureRmApiManagementLogger.md)

[<span data-ttu-id="6d936-146">Remove-Azurermapımanagementgünlükçü</span><span class="sxs-lookup"><span data-stu-id="6d936-146">Remove-AzureRmApiManagementLogger</span></span>](./Remove-AzureRmApiManagementLogger.md)


