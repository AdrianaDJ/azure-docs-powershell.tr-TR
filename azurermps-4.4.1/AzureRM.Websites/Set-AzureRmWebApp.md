---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebApp.md
ms.openlocfilehash: 0f8008a2b567bb2cb2b67755d2ea5bb586f0c115
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588228"
---
# <span data-ttu-id="1893a-101">Set-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="1893a-101">Set-AzureRmWebApp</span></span>

## <span data-ttu-id="1893a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1893a-102">SYNOPSIS</span></span>
<span data-ttu-id="1893a-103">Azure Web App 'i değiştirir.</span><span class="sxs-lookup"><span data-stu-id="1893a-103">Modifies an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1893a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1893a-104">SYNTAX</span></span>

### <span data-ttu-id="1893a-105">S1</span><span class="sxs-lookup"><span data-stu-id="1893a-105">S1</span></span>
```
Set-AzureRmWebApp [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [[-AutoSwapSlotName] <String>] [-HostNames <String[]>] [-NumberOfWorkers <Int32>]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1893a-106">S2</span><span class="sxs-lookup"><span data-stu-id="1893a-106">S2</span></span>
```
Set-AzureRmWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>]
 [-NumberOfWorkers <Int32>] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1893a-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="1893a-107">DESCRIPTION</span></span>
<span data-ttu-id="1893a-108">**Set-AzureRmWebApp** cmdlet 'ı bir Azure Web uygulamasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="1893a-108">The **Set-AzureRmWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="1893a-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1893a-109">EXAMPLES</span></span>

### <span data-ttu-id="1893a-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1893a-110">Example 1</span></span>
```
PS C:\> Set-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="1893a-111">Bu komut, varsayılan-Web-WestUS kaynak grubuyla ilişkili Web App ContosoWebApp için HttpLoggingEnabled true olarak ayarlıyor</span><span class="sxs-lookup"><span data-stu-id="1893a-111">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="1893a-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1893a-112">PARAMETERS</span></span>

### <span data-ttu-id="1893a-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="1893a-113">-AppServicePlan</span></span>
<span data-ttu-id="1893a-114">App Service planı adı</span><span class="sxs-lookup"><span data-stu-id="1893a-114">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1893a-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="1893a-115">-AppSettings</span></span>
<span data-ttu-id="1893a-116">Uygulama ayarları HashTable</span><span class="sxs-lookup"><span data-stu-id="1893a-116">App Settings HashTable</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: S1
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1893a-117">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="1893a-117">-AutoSwapSlotName</span></span>
<span data-ttu-id="1893a-118">Otomatik takas için hedef yuva adı</span><span class="sxs-lookup"><span data-stu-id="1893a-118">Destination slot name for auto swap</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 15
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1893a-119">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="1893a-119">-ConnectionStrings</span></span>
<span data-ttu-id="1893a-120">Bağlantı dizeleri HashTable</span><span class="sxs-lookup"><span data-stu-id="1893a-120">Connection Strings HashTable</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: S1
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1893a-121">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="1893a-121">-DefaultDocuments</span></span>
<span data-ttu-id="1893a-122">Varsayılan belgeler dize dizisi</span><span class="sxs-lookup"><span data-stu-id="1893a-122">Default Documents String Array</span></span>

```yaml
Type: System.String[]
Parameter Sets: S1
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1893a-123">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="1893a-123">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="1893a-124">Ayrıntılı hata günlüğü etkin Boole</span><span class="sxs-lookup"><span data-stu-id="1893a-124">Detailed Error Logging Enabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1893a-125">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="1893a-125">-HandlerMappings</span></span>
<span data-ttu-id="1893a-126">İşleyici eşlemeleri IList</span><span class="sxs-lookup"><span data-stu-id="1893a-126">Handler Mappings IList</span></span>

```yaml
Type: System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]
Parameter Sets: S1
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1893a-127">-Ana makine adları</span><span class="sxs-lookup"><span data-stu-id="1893a-127">-HostNames</span></span>
<span data-ttu-id="1893a-128">WebApp konak adları dize dizisi</span><span class="sxs-lookup"><span data-stu-id="1893a-128">WebApp HostNames String Array</span></span>

```yaml
Type: System.String[]
Parameter Sets: S1
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1893a-129">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="1893a-129">-HttpLoggingEnabled</span></span>
<span data-ttu-id="1893a-130">HttpLoggingEnabled Boolean</span><span class="sxs-lookup"><span data-stu-id="1893a-130">HttpLoggingEnabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1893a-131">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="1893a-131">-ManagedPipelineMode</span></span>
<span data-ttu-id="1893a-132">Yönetilen ardışık düzen modu adı</span><span class="sxs-lookup"><span data-stu-id="1893a-132">Managed Pipeline Mode Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 
Accepted values: Classic, Integrated

Required: False
Position: 12
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1893a-133">-Ad</span><span class="sxs-lookup"><span data-stu-id="1893a-133">-Name</span></span>
<span data-ttu-id="1893a-134">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="1893a-134">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1893a-135">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="1893a-135">-NetFrameworkVersion</span></span>
<span data-ttu-id="1893a-136">NET Framework sürümü</span><span class="sxs-lookup"><span data-stu-id="1893a-136">Net Framework Version</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1893a-137">-Işçilere</span><span class="sxs-lookup"><span data-stu-id="1893a-137">-NumberOfWorkers</span></span>
<span data-ttu-id="1893a-138">Tahsis edilecek çalışan sayısı</span><span class="sxs-lookup"><span data-stu-id="1893a-138">The number of workers to be allocated</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1893a-139">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="1893a-139">-PhpVersion</span></span>
<span data-ttu-id="1893a-140">PHP sürümü</span><span class="sxs-lookup"><span data-stu-id="1893a-140">Php Version</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1893a-141">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="1893a-141">-RequestTracingEnabled</span></span>
<span data-ttu-id="1893a-142">İstek Izleme etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="1893a-142">Request Tracing Enabled</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1893a-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1893a-143">-ResourceGroupName</span></span>
<span data-ttu-id="1893a-144">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="1893a-144">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1893a-145">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="1893a-145">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="1893a-146">32 bit çalışan süreci Boole kullanma</span><span class="sxs-lookup"><span data-stu-id="1893a-146">Use 32-bit Worker Process Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 14
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1893a-147">-WebApp</span><span class="sxs-lookup"><span data-stu-id="1893a-147">-WebApp</span></span>
<span data-ttu-id="1893a-148">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="1893a-148">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1893a-149">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="1893a-149">-WebSocketsEnabled</span></span>
<span data-ttu-id="1893a-150">WebSocketsEnabled Boole değeri</span><span class="sxs-lookup"><span data-stu-id="1893a-150">WebSocketsEnabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: 13
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1893a-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1893a-151">-DefaultProfile</span></span>
<span data-ttu-id="1893a-152">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1893a-152">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1893a-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1893a-153">CommonParameters</span></span>
<span data-ttu-id="1893a-154">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1893a-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1893a-155">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1893a-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1893a-156">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1893a-156">INPUTS</span></span>

### <span data-ttu-id="1893a-157">32</span><span class="sxs-lookup"><span data-stu-id="1893a-157">Int32</span></span>
<span data-ttu-id="1893a-158">' Işçilerin ' parametresi ardışık düzenin ' Int32 ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="1893a-158">Parameter 'NumberOfWorkers' accepts value of type 'Int32' from the pipeline</span></span>

### <span data-ttu-id="1893a-159">Bölge</span><span class="sxs-lookup"><span data-stu-id="1893a-159">Site</span></span>
<span data-ttu-id="1893a-160">' WebApp ' parametresi ardışık düzenin ' site ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="1893a-160">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="1893a-161">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1893a-161">OUTPUTS</span></span>

## <span data-ttu-id="1893a-162">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1893a-162">NOTES</span></span>

## <span data-ttu-id="1893a-163">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1893a-163">RELATED LINKS</span></span>

[<span data-ttu-id="1893a-164">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="1893a-164">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="1893a-165">Yeni-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="1893a-165">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="1893a-166">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="1893a-166">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="1893a-167">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="1893a-167">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="1893a-168">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="1893a-168">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="1893a-169">Stop-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="1893a-169">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)
