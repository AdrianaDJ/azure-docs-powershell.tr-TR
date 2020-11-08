---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5B4ADD38-FA22-4C25-9B9C-FD7861883811
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementLogger.md
ms.openlocfilehash: 6ad32b3bd9bef4f4e684125b280db941da7a7b3f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104180"
---
# <span data-ttu-id="f7011-101">Set-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="f7011-101">Set-AzApiManagementLogger</span></span>

## <span data-ttu-id="f7011-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7011-102">SYNOPSIS</span></span>
<span data-ttu-id="f7011-103">Bir API yönetim günlükçüsü değiştirir.</span><span class="sxs-lookup"><span data-stu-id="f7011-103">Modifies an API Management Logger.</span></span>

## <span data-ttu-id="f7011-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f7011-104">SYNTAX</span></span>

### <span data-ttu-id="f7011-105">EventHubLoggerSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f7011-105">EventHubLoggerSet (Default)</span></span>
```
Set-AzApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-Name <String>]
 [-ConnectionString <String>] [-Description <String>] [-IsBuffered] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7011-106">Applicationınsightsloggerset</span><span class="sxs-lookup"><span data-stu-id="f7011-106">ApplicationInsightsLoggerSet</span></span>
```
Set-AzApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-InstrumentationKey <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f7011-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="f7011-107">DESCRIPTION</span></span>
<span data-ttu-id="f7011-108">**Set-Azapsananagementgünlükçü** cmdlet 'i, BIR Azure API Yönetim **günlükçüsü** ayarlarını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="f7011-108">The **Set-AzApiManagementLogger** cmdlet modifies settings of an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="f7011-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f7011-109">EXAMPLES</span></span>

### <span data-ttu-id="f7011-110">Örnek 1: EventHub günlükçüsü değiştirme</span><span class="sxs-lookup"><span data-stu-id="f7011-110">Example 1: Modify EventHub logger</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementLogger -Context $apimContext -LoggerId "Logger123" -Name "ContosoSdkEventHub" -ConnectionString "Endpoint=sb://ContosoSdkEventHubs.servicebus.windows.net/;SharedAccessKeyName=SendKey;SharedAccessKey=<key>" -Description "updated SDK event hub logger" -PassThru
```

<span data-ttu-id="f7011-111">Bu komut, KIMLIĞI Logger123 olan bir günlükçüsü değiştirir.</span><span class="sxs-lookup"><span data-stu-id="f7011-111">This command modifies a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="f7011-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f7011-112">PARAMETERS</span></span>

### <span data-ttu-id="f7011-113">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="f7011-113">-ConnectionString</span></span>
<span data-ttu-id="f7011-114">İlke haklarını içeren bir Azure etkinliği hub bağlantı dizesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f7011-114">Specifies an Azure Event Hubs connection string that includes Send policy rights.</span></span>

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

### <span data-ttu-id="f7011-115">-Context</span><span class="sxs-lookup"><span data-stu-id="f7011-115">-Context</span></span>
<span data-ttu-id="f7011-116">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f7011-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="f7011-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7011-117">-DefaultProfile</span></span>
<span data-ttu-id="f7011-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f7011-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7011-119">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="f7011-119">-Description</span></span>
<span data-ttu-id="f7011-120">Bir açıklama belirtir.</span><span class="sxs-lookup"><span data-stu-id="f7011-120">Specifies a description.</span></span>

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

### <span data-ttu-id="f7011-121">-Enstrüentationkey</span><span class="sxs-lookup"><span data-stu-id="f7011-121">-InstrumentationKey</span></span>
<span data-ttu-id="f7011-122">Application Insights 'ın alt yapısı.</span><span class="sxs-lookup"><span data-stu-id="f7011-122">Instrumentation Key of the application Insights.</span></span> <span data-ttu-id="f7011-123">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="f7011-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="f7011-124">-Isarabellekli</span><span class="sxs-lookup"><span data-stu-id="f7011-124">-IsBuffered</span></span>
<span data-ttu-id="f7011-125">Kayıt defterinde, yayımlamadan önce arabelleğe alınan kayıtların arabelleğe alınıp alınmayacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f7011-125">Specifies that the records in the logger are buffered before publishing.</span></span>
<span data-ttu-id="f7011-126">Kayıtlar arabelleğe alındıklarında, her 15 saniyede bir olay hublara veya arabellek 256 KB ileti aldığında gönderilir.</span><span class="sxs-lookup"><span data-stu-id="f7011-126">When records are buffered, they are sent to Event Hubs every 15 seconds, or whenever the buffer receives 256 KB of messages.</span></span>

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

### <span data-ttu-id="f7011-127">-Loggerıd</span><span class="sxs-lookup"><span data-stu-id="f7011-127">-LoggerId</span></span>
<span data-ttu-id="f7011-128">Güncelleştirilecek günlükçü KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="f7011-128">Specifies the ID of the logger to update.</span></span>

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

### <span data-ttu-id="f7011-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="f7011-129">-Name</span></span>
<span data-ttu-id="f7011-130">Azure Classic Portal 'dan bir olay hub 'ının varlık adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f7011-130">Specifies the entity name of an event hub from Azure classic portal.</span></span>

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

### <span data-ttu-id="f7011-131">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="f7011-131">-PassThru</span></span>
<span data-ttu-id="f7011-132">Bu cmdlet 'in değiştirdiği  **Psapsananagementgünlükçü** değerini geri aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f7011-132">Indicates that this cmdlet returns the  **PsApiManagementLogger** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="f7011-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="f7011-133">-Confirm</span></span>
<span data-ttu-id="f7011-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f7011-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7011-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7011-135">-WhatIf</span></span>
<span data-ttu-id="f7011-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f7011-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f7011-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f7011-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7011-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7011-138">CommonParameters</span></span>
<span data-ttu-id="f7011-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f7011-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7011-140">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="f7011-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7011-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f7011-141">INPUTS</span></span>

### <span data-ttu-id="f7011-142">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="f7011-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f7011-143">System. String</span><span class="sxs-lookup"><span data-stu-id="f7011-143">System.String</span></span>

### <span data-ttu-id="f7011-144">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f7011-144">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f7011-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f7011-145">OUTPUTS</span></span>

### <span data-ttu-id="f7011-146">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementgünlükçü</span><span class="sxs-lookup"><span data-stu-id="f7011-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="f7011-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f7011-147">NOTES</span></span>

## <span data-ttu-id="f7011-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f7011-148">RELATED LINKS</span></span>

[<span data-ttu-id="f7011-149">Get-Azapsananagementgünlükçü</span><span class="sxs-lookup"><span data-stu-id="f7011-149">Get-AzApiManagementLogger</span></span>](./Get-AzApiManagementLogger.md)

[<span data-ttu-id="f7011-150">Yeni-Azsız</span><span class="sxs-lookup"><span data-stu-id="f7011-150">New-AzApiManagementLogger</span></span>](./New-AzApiManagementLogger.md)

[<span data-ttu-id="f7011-151">Remove-Azapsananagementgünlükçü</span><span class="sxs-lookup"><span data-stu-id="f7011-151">Remove-AzApiManagementLogger</span></span>](./Remove-AzApiManagementLogger.md)


