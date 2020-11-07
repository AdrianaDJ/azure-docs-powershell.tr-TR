---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5B4ADD38-FA22-4C25-9B9C-FD7861883811
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementLogger.md
ms.openlocfilehash: 4c7f4b4f308d04c6f9c82e70f9fbe0598bd4a9fb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917687"
---
# <span data-ttu-id="f7b3f-101">Set-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="f7b3f-101">Set-AzApiManagementLogger</span></span>

## <span data-ttu-id="f7b3f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7b3f-102">SYNOPSIS</span></span>
<span data-ttu-id="f7b3f-103">Bir API yönetim günlükçüsü değiştirir.</span><span class="sxs-lookup"><span data-stu-id="f7b3f-103">Modifies an API Management Logger.</span></span>

## <span data-ttu-id="f7b3f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f7b3f-104">SYNTAX</span></span>

### <span data-ttu-id="f7b3f-105">EventHubLoggerSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f7b3f-105">EventHubLoggerSet (Default)</span></span>
```
Set-AzApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-Name <String>]
 [-ConnectionString <String>] [-Description <String>] [-IsBuffered] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7b3f-106">Applicationınsightsloggerset</span><span class="sxs-lookup"><span data-stu-id="f7b3f-106">ApplicationInsightsLoggerSet</span></span>
```
Set-AzApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-InstrumentationKey <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7b3f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="f7b3f-107">DESCRIPTION</span></span>
<span data-ttu-id="f7b3f-108">**Set-Azapsananagementgünlükçü** cmdlet 'i, BIR Azure API Yönetim **günlükçüsü** ayarlarını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="f7b3f-108">The **Set-AzApiManagementLogger** cmdlet modifies settings of an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="f7b3f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f7b3f-109">EXAMPLES</span></span>

### <span data-ttu-id="f7b3f-110">Örnek 1: EventHub günlükçüsü değiştirme</span><span class="sxs-lookup"><span data-stu-id="f7b3f-110">Example 1: Modify EventHub logger</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementLogger -Context $apimContext -LoggerId "Logger123" -Name "ContosoSdkEventHub" -ConnectionString "Endpoint=sb://ContosoSdkEventHubs.servicebus.windows.net/;SharedAccessKeyName=SendKey;SharedAccessKey=<key>" -Description "updated SDK event hub logger" -PassThru
```

<span data-ttu-id="f7b3f-111">Bu komut, KIMLIĞI Logger123 olan bir günlükçüsü değiştirir.</span><span class="sxs-lookup"><span data-stu-id="f7b3f-111">This command modifies a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="f7b3f-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f7b3f-112">PARAMETERS</span></span>

### <span data-ttu-id="f7b3f-113">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="f7b3f-113">-ConnectionString</span></span>
<span data-ttu-id="f7b3f-114">İlke haklarını içeren bir Azure etkinliği hub bağlantı dizesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f7b3f-114">Specifies an Azure Event Hubs connection string that includes Send policy rights.</span></span>

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

### <span data-ttu-id="f7b3f-115">-Context</span><span class="sxs-lookup"><span data-stu-id="f7b3f-115">-Context</span></span>
<span data-ttu-id="f7b3f-116">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f7b3f-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="f7b3f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7b3f-117">-DefaultProfile</span></span>
<span data-ttu-id="f7b3f-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f7b3f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7b3f-119">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="f7b3f-119">-Description</span></span>
<span data-ttu-id="f7b3f-120">Bir açıklama belirtir.</span><span class="sxs-lookup"><span data-stu-id="f7b3f-120">Specifies a description.</span></span>

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

### <span data-ttu-id="f7b3f-121">-Enstrüentationkey</span><span class="sxs-lookup"><span data-stu-id="f7b3f-121">-InstrumentationKey</span></span>
<span data-ttu-id="f7b3f-122">Application Insights 'ın alt yapısı.</span><span class="sxs-lookup"><span data-stu-id="f7b3f-122">Instrumentation Key of the application Insights.</span></span> <span data-ttu-id="f7b3f-123">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="f7b3f-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="f7b3f-124">-Isarabellekli</span><span class="sxs-lookup"><span data-stu-id="f7b3f-124">-IsBuffered</span></span>
<span data-ttu-id="f7b3f-125">Kayıt defterinde, yayımlamadan önce arabelleğe alınan kayıtların arabelleğe alınıp alınmayacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f7b3f-125">Specifies that the records in the logger are buffered before publishing.</span></span>
<span data-ttu-id="f7b3f-126">Kayıtlar arabelleğe alındıklarında, her 15 saniyede bir olay hublara veya arabellek 256 KB ileti aldığında gönderilir.</span><span class="sxs-lookup"><span data-stu-id="f7b3f-126">When records are buffered, they are sent to Event Hubs every 15 seconds, or whenever the buffer receives 256 KB of messages.</span></span>

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

### <span data-ttu-id="f7b3f-127">-Loggerıd</span><span class="sxs-lookup"><span data-stu-id="f7b3f-127">-LoggerId</span></span>
<span data-ttu-id="f7b3f-128">Güncelleştirilecek günlükçü KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="f7b3f-128">Specifies the ID of the logger to update.</span></span>

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

### <span data-ttu-id="f7b3f-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="f7b3f-129">-Name</span></span>
<span data-ttu-id="f7b3f-130">Azure Classic Portal 'dan bir olay hub 'ının varlık adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f7b3f-130">Specifies the entity name of an event hub from Azure classic portal.</span></span>

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

### <span data-ttu-id="f7b3f-131">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="f7b3f-131">-PassThru</span></span>
<span data-ttu-id="f7b3f-132">Bu cmdlet 'in değiştirdiği  **Psapsananagementgünlükçü** değerini geri aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f7b3f-132">Indicates that this cmdlet returns the  **PsApiManagementLogger** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="f7b3f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7b3f-133">CommonParameters</span></span>
<span data-ttu-id="f7b3f-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f7b3f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7b3f-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7b3f-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7b3f-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f7b3f-136">INPUTS</span></span>

### <span data-ttu-id="f7b3f-137">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="f7b3f-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f7b3f-138">System. String</span><span class="sxs-lookup"><span data-stu-id="f7b3f-138">System.String</span></span>

### <span data-ttu-id="f7b3f-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f7b3f-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f7b3f-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f7b3f-140">OUTPUTS</span></span>

### <span data-ttu-id="f7b3f-141">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementgünlükçü</span><span class="sxs-lookup"><span data-stu-id="f7b3f-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="f7b3f-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f7b3f-142">NOTES</span></span>

## <span data-ttu-id="f7b3f-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f7b3f-143">RELATED LINKS</span></span>

[<span data-ttu-id="f7b3f-144">Get-Azapsananagementgünlükçü</span><span class="sxs-lookup"><span data-stu-id="f7b3f-144">Get-AzApiManagementLogger</span></span>](./Get-AzApiManagementLogger.md)

[<span data-ttu-id="f7b3f-145">Yeni-Azsız</span><span class="sxs-lookup"><span data-stu-id="f7b3f-145">New-AzApiManagementLogger</span></span>](./New-AzApiManagementLogger.md)

[<span data-ttu-id="f7b3f-146">Remove-Azapsananagementgünlükçü</span><span class="sxs-lookup"><span data-stu-id="f7b3f-146">Remove-AzApiManagementLogger</span></span>](./Remove-AzApiManagementLogger.md)


