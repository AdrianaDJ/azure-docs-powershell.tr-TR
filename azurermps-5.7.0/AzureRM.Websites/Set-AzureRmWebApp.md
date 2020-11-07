---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/set-azurermwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebApp.md
ms.openlocfilehash: 3587c7a725386976a04a9dc9922b3b0a16eb9362
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593351"
---
# <span data-ttu-id="047e3-101">Set-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="047e3-101">Set-AzureRmWebApp</span></span>

## <span data-ttu-id="047e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="047e3-102">SYNOPSIS</span></span>
<span data-ttu-id="047e3-103">Azure Web App 'i değiştirir.</span><span class="sxs-lookup"><span data-stu-id="047e3-103">Modifies an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="047e3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="047e3-104">SYNTAX</span></span>

### <span data-ttu-id="047e3-105">S1</span><span class="sxs-lookup"><span data-stu-id="047e3-105">S1</span></span>
```
Set-AzureRmWebApp [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [[-AutoSwapSlotName] <String>] [-HostNames <String[]>] [-NumberOfWorkers <Int32>]
 [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="047e3-106">S2</span><span class="sxs-lookup"><span data-stu-id="047e3-106">S2</span></span>
```
Set-AzureRmWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>]
 [-NumberOfWorkers <Int32>] [-WebApp] <Site> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="047e3-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="047e3-107">DESCRIPTION</span></span>
<span data-ttu-id="047e3-108">**Set-AzureRmWebApp** cmdlet 'ı bir Azure Web uygulamasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="047e3-108">The **Set-AzureRmWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="047e3-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="047e3-109">EXAMPLES</span></span>

### <span data-ttu-id="047e3-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="047e3-110">Example 1</span></span>
```
PS C:\> Set-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="047e3-111">Bu komut, varsayılan-Web-WestUS kaynak grubuyla ilişkili Web App ContosoWebApp için HttpLoggingEnabled true olarak ayarlıyor</span><span class="sxs-lookup"><span data-stu-id="047e3-111">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="047e3-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="047e3-112">PARAMETERS</span></span>

### <span data-ttu-id="047e3-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="047e3-113">-AppServicePlan</span></span>
<span data-ttu-id="047e3-114">App Service planı adı</span><span class="sxs-lookup"><span data-stu-id="047e3-114">App Service Plan Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="047e3-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="047e3-115">-AppSettings</span></span>
<span data-ttu-id="047e3-116">Uygulama ayarları HashTable</span><span class="sxs-lookup"><span data-stu-id="047e3-116">App Settings HashTable</span></span>

```yaml
Type: Hashtable
Parameter Sets: S1
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="047e3-117">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="047e3-117">-AutoSwapSlotName</span></span>
<span data-ttu-id="047e3-118">Otomatik takas için hedef yuva adı</span><span class="sxs-lookup"><span data-stu-id="047e3-118">Destination slot name for auto swap</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 15
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="047e3-119">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="047e3-119">-ConnectionStrings</span></span>
<span data-ttu-id="047e3-120">Bağlantı dizeleri HashTable</span><span class="sxs-lookup"><span data-stu-id="047e3-120">Connection Strings HashTable</span></span>

```yaml
Type: Hashtable
Parameter Sets: S1
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="047e3-121">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="047e3-121">-DefaultDocuments</span></span>
<span data-ttu-id="047e3-122">Varsayılan belgeler dize dizisi</span><span class="sxs-lookup"><span data-stu-id="047e3-122">Default Documents String Array</span></span>

```yaml
Type: String[]
Parameter Sets: S1
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="047e3-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="047e3-123">-DefaultProfile</span></span>
<span data-ttu-id="047e3-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="047e3-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="047e3-125">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="047e3-125">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="047e3-126">Ayrıntılı hata günlüğü etkin Boole</span><span class="sxs-lookup"><span data-stu-id="047e3-126">Detailed Error Logging Enabled Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="047e3-127">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="047e3-127">-HandlerMappings</span></span>
<span data-ttu-id="047e3-128">İşleyici eşlemeleri IList</span><span class="sxs-lookup"><span data-stu-id="047e3-128">Handler Mappings IList</span></span>

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

### <span data-ttu-id="047e3-129">-Ana makine adları</span><span class="sxs-lookup"><span data-stu-id="047e3-129">-HostNames</span></span>
<span data-ttu-id="047e3-130">WebApp konak adları dize dizisi</span><span class="sxs-lookup"><span data-stu-id="047e3-130">WebApp HostNames String Array</span></span>

```yaml
Type: String[]
Parameter Sets: S1
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="047e3-131">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="047e3-131">-HttpLoggingEnabled</span></span>
<span data-ttu-id="047e3-132">HttpLoggingEnabled Boolean</span><span class="sxs-lookup"><span data-stu-id="047e3-132">HttpLoggingEnabled Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="047e3-133">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="047e3-133">-ManagedPipelineMode</span></span>
<span data-ttu-id="047e3-134">Yönetilen ardışık düzen modu adı</span><span class="sxs-lookup"><span data-stu-id="047e3-134">Managed Pipeline Mode Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 
Accepted values: Classic, Integrated

Required: False
Position: 12
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="047e3-135">-Ad</span><span class="sxs-lookup"><span data-stu-id="047e3-135">-Name</span></span>
<span data-ttu-id="047e3-136">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="047e3-136">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="047e3-137">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="047e3-137">-NetFrameworkVersion</span></span>
<span data-ttu-id="047e3-138">NET Framework sürümü</span><span class="sxs-lookup"><span data-stu-id="047e3-138">Net Framework Version</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="047e3-139">-Işçilere</span><span class="sxs-lookup"><span data-stu-id="047e3-139">-NumberOfWorkers</span></span>
<span data-ttu-id="047e3-140">Tahsis edilecek çalışan sayısı</span><span class="sxs-lookup"><span data-stu-id="047e3-140">The number of workers to be allocated</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="047e3-141">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="047e3-141">-PhpVersion</span></span>
<span data-ttu-id="047e3-142">PHP sürümü</span><span class="sxs-lookup"><span data-stu-id="047e3-142">Php Version</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="047e3-143">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="047e3-143">-RequestTracingEnabled</span></span>
<span data-ttu-id="047e3-144">İstek Izleme etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="047e3-144">Request Tracing Enabled</span></span>

```yaml
Type: Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="047e3-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="047e3-145">-ResourceGroupName</span></span>
<span data-ttu-id="047e3-146">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="047e3-146">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="047e3-147">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="047e3-147">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="047e3-148">32 bit çalışan süreci Boole kullanma</span><span class="sxs-lookup"><span data-stu-id="047e3-148">Use 32-bit Worker Process Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 14
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="047e3-149">-WebApp</span><span class="sxs-lookup"><span data-stu-id="047e3-149">-WebApp</span></span>
<span data-ttu-id="047e3-150">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="047e3-150">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="047e3-151">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="047e3-151">-WebSocketsEnabled</span></span>
<span data-ttu-id="047e3-152">WebSocketsEnabled Boole değeri</span><span class="sxs-lookup"><span data-stu-id="047e3-152">WebSocketsEnabled Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: 13
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="047e3-153">-Iş</span><span class="sxs-lookup"><span data-stu-id="047e3-153">-AsJob</span></span>
<span data-ttu-id="047e3-154">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="047e3-154">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="047e3-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="047e3-155">CommonParameters</span></span>
<span data-ttu-id="047e3-156">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="047e3-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="047e3-157">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="047e3-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="047e3-158">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="047e3-158">INPUTS</span></span>

### <span data-ttu-id="047e3-159">32</span><span class="sxs-lookup"><span data-stu-id="047e3-159">Int32</span></span>
<span data-ttu-id="047e3-160">' Işçilerin ' parametresi ardışık düzenin ' Int32 ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="047e3-160">Parameter 'NumberOfWorkers' accepts value of type 'Int32' from the pipeline</span></span>

### <span data-ttu-id="047e3-161">Bölge</span><span class="sxs-lookup"><span data-stu-id="047e3-161">Site</span></span>
<span data-ttu-id="047e3-162">' WebApp ' parametresi ardışık düzenin ' site ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="047e3-162">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="047e3-163">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="047e3-163">OUTPUTS</span></span>

## <span data-ttu-id="047e3-164">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="047e3-164">NOTES</span></span>

## <span data-ttu-id="047e3-165">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="047e3-165">RELATED LINKS</span></span>

[<span data-ttu-id="047e3-166">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="047e3-166">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="047e3-167">Yeni-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="047e3-167">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="047e3-168">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="047e3-168">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="047e3-169">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="047e3-169">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="047e3-170">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="047e3-170">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="047e3-171">Stop-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="047e3-171">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)