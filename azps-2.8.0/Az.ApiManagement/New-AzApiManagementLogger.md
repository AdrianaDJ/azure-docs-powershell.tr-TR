---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 17D53F56-6E3B-491E-8776-5EBE109FBE3C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementLogger.md
ms.openlocfilehash: c1ddf2ec1e83a73d130f5be5eee38bfc8cac4c9a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753517"
---
# <span data-ttu-id="ca3f4-101">New-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="ca3f4-101">New-AzApiManagementLogger</span></span>

## <span data-ttu-id="ca3f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca3f4-102">SYNOPSIS</span></span>
<span data-ttu-id="ca3f4-103">Bir API yönetim günlükçüsü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ca3f4-103">Creates an API Management Logger.</span></span>

## <span data-ttu-id="ca3f4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ca3f4-104">SYNTAX</span></span>

### <span data-ttu-id="ca3f4-105">EventHubLoggerSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ca3f4-105">EventHubLoggerSet (Default)</span></span>
```
New-AzApiManagementLogger -Context <PsApiManagementContext> [-LoggerId <String>] -Name <String>
 -ConnectionString <String> [-Description <String>] [-IsBuffered <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ca3f4-106">Applicationınsightsloggerset</span><span class="sxs-lookup"><span data-stu-id="ca3f4-106">ApplicationInsightsLoggerSet</span></span>
```
New-AzApiManagementLogger -Context <PsApiManagementContext> [-LoggerId <String>] -InstrumentationKey <String>
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ca3f4-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="ca3f4-107">DESCRIPTION</span></span>
<span data-ttu-id="ca3f4-108">**Yeni-Azapsananagementgünlükçü** cmdlet 'ı BIR Azure API Yönetim **günlükçüsü** oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ca3f4-108">The **New-AzApiManagementLogger** cmdlet creates an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="ca3f4-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ca3f4-109">EXAMPLES</span></span>

### <span data-ttu-id="ca3f4-110">Örnek 1: günlükçü oluşturma</span><span class="sxs-lookup"><span data-stu-id="ca3f4-110">Example 1: Create a logger</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementLogger -Context $apimContext -LoggerId "Logger123" -Name "ContosoSdkEventHub" -ConnectionString "Endpoint=sb://ContosoSdkEventHubs.servicebus.windows.net/;SharedAccessKeyName=SendKey;SharedAccessKey=<key>" -Description "SDK event hub logger"
```

<span data-ttu-id="ca3f4-111">Bu komut, belirtilen bağlantı dizesini kullanarak ContosoSdkEventHub adlı bir günlükçü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ca3f4-111">This command creates a logger named ContosoSdkEventHub by using the specified connection string.</span></span>

## <span data-ttu-id="ca3f4-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ca3f4-112">PARAMETERS</span></span>

### <span data-ttu-id="ca3f4-113">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="ca3f4-113">-ConnectionString</span></span>
<span data-ttu-id="ca3f4-114">Aşağıdakiler ile başlayan bir Azure Olay Hub bağlantı dizesi belirtir: `Endpoint=endpoint and key from Azure classic portal`</span><span class="sxs-lookup"><span data-stu-id="ca3f4-114">Specifies an Azure Event Hubs connection string that starts with the following: `Endpoint=endpoint and key from Azure classic portal`</span></span>
<span data-ttu-id="ca3f4-115">Bağlantı dizesindeki gönderme haklarını içeren anahtar yapılandırılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="ca3f4-115">The Key with Send Rights in the connection string must be configured.</span></span>

```yaml
Type: System.String
Parameter Sets: EventHubLoggerSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca3f4-116">-Context</span><span class="sxs-lookup"><span data-stu-id="ca3f4-116">-Context</span></span>
<span data-ttu-id="ca3f4-117">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ca3f4-117">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="ca3f4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca3f4-118">-DefaultProfile</span></span>
<span data-ttu-id="ca3f4-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ca3f4-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ca3f4-120">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="ca3f4-120">-Description</span></span>
<span data-ttu-id="ca3f4-121">Bir açıklama belirtir.</span><span class="sxs-lookup"><span data-stu-id="ca3f4-121">Specifies a description.</span></span>

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

### <span data-ttu-id="ca3f4-122">-Enstrüentationkey</span><span class="sxs-lookup"><span data-stu-id="ca3f4-122">-InstrumentationKey</span></span>
<span data-ttu-id="ca3f4-123">Application Insights 'ın alt yapısı.</span><span class="sxs-lookup"><span data-stu-id="ca3f4-123">Instrumentation Key of the application Insights.</span></span> <span data-ttu-id="ca3f4-124">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="ca3f4-124">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationInsightsLoggerSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca3f4-125">-Isarabellekli</span><span class="sxs-lookup"><span data-stu-id="ca3f4-125">-IsBuffered</span></span>
<span data-ttu-id="ca3f4-126">Kayıt defterinde, yayımlamadan önce arabelleğe alınıp alınmadığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ca3f4-126">Specifies whether the records in the logger are buffered before publishing.</span></span>
<span data-ttu-id="ca3f4-127">Varsayılan değer $True.</span><span class="sxs-lookup"><span data-stu-id="ca3f4-127">The default value is $True.</span></span>
<span data-ttu-id="ca3f4-128">Kayıtlar arabelleğe alındıklarında, her 15 saniyede bir olay hublara veya arabellek 256 KB ileti aldığında gönderilir.</span><span class="sxs-lookup"><span data-stu-id="ca3f4-128">When records are buffered, they are sent to Event Hubs every 15 seconds, or whenever the buffer receives 256 KB of messages.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: EventHubLoggerSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca3f4-129">-Loggerıd</span><span class="sxs-lookup"><span data-stu-id="ca3f4-129">-LoggerId</span></span>
<span data-ttu-id="ca3f4-130">Günlükçü için bir KIMLIK belirtir.</span><span class="sxs-lookup"><span data-stu-id="ca3f4-130">Specifies an ID for the logger.</span></span>
<span data-ttu-id="ca3f4-131">KIMLIK belirtmezseniz, bu cmdlet bir tane oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ca3f4-131">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="ca3f4-132">-Ad</span><span class="sxs-lookup"><span data-stu-id="ca3f4-132">-Name</span></span>
<span data-ttu-id="ca3f4-133">Azure Classic Portal 'dan bir olay hub 'ının varlık adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ca3f4-133">Specifies the entity name of an event hub from Azure classic portal.</span></span>

```yaml
Type: System.String
Parameter Sets: EventHubLoggerSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca3f4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca3f4-134">CommonParameters</span></span>
<span data-ttu-id="ca3f4-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ca3f4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca3f4-136">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ca3f4-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca3f4-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ca3f4-137">INPUTS</span></span>

### <span data-ttu-id="ca3f4-138">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="ca3f4-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ca3f4-139">System. String</span><span class="sxs-lookup"><span data-stu-id="ca3f4-139">System.String</span></span>

### <span data-ttu-id="ca3f4-140">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="ca3f4-140">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="ca3f4-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ca3f4-141">OUTPUTS</span></span>

### <span data-ttu-id="ca3f4-142">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementgünlükçü</span><span class="sxs-lookup"><span data-stu-id="ca3f4-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="ca3f4-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ca3f4-143">NOTES</span></span>

## <span data-ttu-id="ca3f4-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ca3f4-144">RELATED LINKS</span></span>

[<span data-ttu-id="ca3f4-145">Get-Azapsananagementgünlükçü</span><span class="sxs-lookup"><span data-stu-id="ca3f4-145">Get-AzApiManagementLogger</span></span>](./Get-AzApiManagementLogger.md)

[<span data-ttu-id="ca3f4-146">Remove-Azapsananagementgünlükçü</span><span class="sxs-lookup"><span data-stu-id="ca3f4-146">Remove-AzApiManagementLogger</span></span>](./Remove-AzApiManagementLogger.md)

[<span data-ttu-id="ca3f4-147">Set-Azapsananagementgünlükçü</span><span class="sxs-lookup"><span data-stu-id="ca3f4-147">Set-AzApiManagementLogger</span></span>](./Set-AzApiManagementLogger.md)


