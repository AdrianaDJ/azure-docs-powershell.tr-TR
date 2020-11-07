---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/set-Azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Set-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Set-AzWebApp.md
ms.openlocfilehash: 4478083a2ee98eceda08012b4346f3ece1657963
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936062"
---
# <span data-ttu-id="8155b-101">Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="8155b-101">Set-AzWebApp</span></span>

## <span data-ttu-id="8155b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8155b-102">SYNOPSIS</span></span>
<span data-ttu-id="8155b-103">Azure Web App 'i değiştirir.</span><span class="sxs-lookup"><span data-stu-id="8155b-103">Modifies an Azure Web App.</span></span>

## <span data-ttu-id="8155b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8155b-104">SYNTAX</span></span>

### <span data-ttu-id="8155b-105">S1</span><span class="sxs-lookup"><span data-stu-id="8155b-105">S1</span></span>
```
Set-AzWebApp [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [[-AutoSwapSlotName] <String>] [-HostNames <String[]>] [-NumberOfWorkers <Int32>] [-AsJob] [[-AssignIdentity] <Boolean>]
 [[-HttpsOnly] <Boolean>] [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8155b-106">S2</span><span class="sxs-lookup"><span data-stu-id="8155b-106">S2</span></span>
```
Set-AzWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>]
 [-NumberOfWorkers <Int32>] [-AsJob] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8155b-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="8155b-107">DESCRIPTION</span></span>
<span data-ttu-id="8155b-108">**Set-AzWebApp** cmdlet 'ı bir Azure Web uygulamasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="8155b-108">The **Set-AzWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="8155b-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8155b-109">EXAMPLES</span></span>

### <span data-ttu-id="8155b-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="8155b-110">Example 1</span></span>
```
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="8155b-111">Bu komut, varsayılan-Web-WestUS kaynak grubuyla ilişkili Web App ContosoWebApp için HttpLoggingEnabled true olarak ayarlıyor</span><span class="sxs-lookup"><span data-stu-id="8155b-111">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="8155b-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8155b-112">PARAMETERS</span></span>

### <span data-ttu-id="8155b-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="8155b-113">-AppServicePlan</span></span>
<span data-ttu-id="8155b-114">App Service planı adı</span><span class="sxs-lookup"><span data-stu-id="8155b-114">App Service Plan Name</span></span>

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

### <span data-ttu-id="8155b-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="8155b-115">-AppSettings</span></span>
<span data-ttu-id="8155b-116">Uygulama ayarları HashTable</span><span class="sxs-lookup"><span data-stu-id="8155b-116">App Settings HashTable</span></span>

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

### <span data-ttu-id="8155b-117">-Iş</span><span class="sxs-lookup"><span data-stu-id="8155b-117">-AsJob</span></span>
<span data-ttu-id="8155b-118">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="8155b-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8155b-119">-Atama kimliği</span><span class="sxs-lookup"><span data-stu-id="8155b-119">-AssignIdentity</span></span>
<span data-ttu-id="8155b-120">Mevcut Azure WebApp veya functionapp 'te MSI 'yi etkinleştirme/devre dışı bırakma [ÖNIZLEME]</span><span class="sxs-lookup"><span data-stu-id="8155b-120">Enable/disable MSI on an existing azure webapp or functionapp [PREVIEW]</span></span>

```yaml
Type: Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8155b-121">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="8155b-121">-AutoSwapSlotName</span></span>
<span data-ttu-id="8155b-122">Otomatik takas için hedef yuva adı</span><span class="sxs-lookup"><span data-stu-id="8155b-122">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="8155b-123">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="8155b-123">-ConnectionStrings</span></span>
<span data-ttu-id="8155b-124">Bağlantı dizeleri HashTable</span><span class="sxs-lookup"><span data-stu-id="8155b-124">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="8155b-125">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="8155b-125">-DefaultDocuments</span></span>
<span data-ttu-id="8155b-126">Varsayılan belgeler dize dizisi</span><span class="sxs-lookup"><span data-stu-id="8155b-126">Default Documents String Array</span></span>

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

### <span data-ttu-id="8155b-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8155b-127">-DefaultProfile</span></span>
<span data-ttu-id="8155b-128">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8155b-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8155b-129">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="8155b-129">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="8155b-130">Ayrıntılı hata günlüğü etkin Boole</span><span class="sxs-lookup"><span data-stu-id="8155b-130">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="8155b-131">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="8155b-131">-HandlerMappings</span></span>
<span data-ttu-id="8155b-132">İşleyici eşlemeleri IList</span><span class="sxs-lookup"><span data-stu-id="8155b-132">Handler Mappings IList</span></span>

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

### <span data-ttu-id="8155b-133">-Ana makine adları</span><span class="sxs-lookup"><span data-stu-id="8155b-133">-HostNames</span></span>
<span data-ttu-id="8155b-134">WebApp konak adları dize dizisi</span><span class="sxs-lookup"><span data-stu-id="8155b-134">WebApp HostNames String Array</span></span>

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

### <span data-ttu-id="8155b-135">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="8155b-135">-HttpLoggingEnabled</span></span>
<span data-ttu-id="8155b-136">HttpLoggingEnabled Boolean</span><span class="sxs-lookup"><span data-stu-id="8155b-136">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="8155b-137">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="8155b-137">-HttpsOnly</span></span>
<span data-ttu-id="8155b-138">Var olan Azure WebApp veya functionapp 'te tüm trafiği HTTPS 'ye yönlendirmeyi etkinleştirme/devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="8155b-138">Enable/disable redirecting all traffic to HTTPS on an existing azure webapp or functionapp</span></span>

```yaml
Type: Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8155b-139">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="8155b-139">-ManagedPipelineMode</span></span>
<span data-ttu-id="8155b-140">Yönetilen ardışık düzen modu adı</span><span class="sxs-lookup"><span data-stu-id="8155b-140">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="8155b-141">-Ad</span><span class="sxs-lookup"><span data-stu-id="8155b-141">-Name</span></span>
<span data-ttu-id="8155b-142">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="8155b-142">WebApp Name</span></span>

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

### <span data-ttu-id="8155b-143">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="8155b-143">-NetFrameworkVersion</span></span>
<span data-ttu-id="8155b-144">NET Framework sürümü</span><span class="sxs-lookup"><span data-stu-id="8155b-144">Net Framework Version</span></span>

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

### <span data-ttu-id="8155b-145">-Işçilere</span><span class="sxs-lookup"><span data-stu-id="8155b-145">-NumberOfWorkers</span></span>
<span data-ttu-id="8155b-146">Tahsis edilecek çalışan sayısı</span><span class="sxs-lookup"><span data-stu-id="8155b-146">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="8155b-147">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="8155b-147">-PhpVersion</span></span>
<span data-ttu-id="8155b-148">PHP sürümü</span><span class="sxs-lookup"><span data-stu-id="8155b-148">Php Version</span></span>

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

### <span data-ttu-id="8155b-149">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="8155b-149">-RequestTracingEnabled</span></span>
<span data-ttu-id="8155b-150">İstek Izleme etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="8155b-150">Request Tracing Enabled</span></span>

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

### <span data-ttu-id="8155b-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8155b-151">-ResourceGroupName</span></span>
<span data-ttu-id="8155b-152">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="8155b-152">Resource Group Name</span></span>

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

### <span data-ttu-id="8155b-153">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="8155b-153">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="8155b-154">32 bit çalışan süreci Boole kullanma</span><span class="sxs-lookup"><span data-stu-id="8155b-154">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="8155b-155">-WebApp</span><span class="sxs-lookup"><span data-stu-id="8155b-155">-WebApp</span></span>
<span data-ttu-id="8155b-156">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="8155b-156">WebApp Object</span></span>

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

### <span data-ttu-id="8155b-157">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="8155b-157">-WebSocketsEnabled</span></span>
<span data-ttu-id="8155b-158">WebSocketsEnabled Boole değeri</span><span class="sxs-lookup"><span data-stu-id="8155b-158">WebSocketsEnabled Boolean</span></span>

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

### <span data-ttu-id="8155b-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8155b-159">CommonParameters</span></span>
<span data-ttu-id="8155b-160">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8155b-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8155b-161">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8155b-161">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8155b-162">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8155b-162">INPUTS</span></span>

### <span data-ttu-id="8155b-163">32</span><span class="sxs-lookup"><span data-stu-id="8155b-163">Int32</span></span>
<span data-ttu-id="8155b-164">' Işçilerin ' parametresi ardışık düzenin ' Int32 ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="8155b-164">Parameter 'NumberOfWorkers' accepts value of type 'Int32' from the pipeline</span></span>

### <span data-ttu-id="8155b-165">Bölge</span><span class="sxs-lookup"><span data-stu-id="8155b-165">Site</span></span>
<span data-ttu-id="8155b-166">' WebApp ' parametresi ardışık düzenin ' site ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="8155b-166">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="8155b-167">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8155b-167">OUTPUTS</span></span>

## <span data-ttu-id="8155b-168">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8155b-168">NOTES</span></span>

## <span data-ttu-id="8155b-169">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8155b-169">RELATED LINKS</span></span>

[<span data-ttu-id="8155b-170">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="8155b-170">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="8155b-171">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="8155b-171">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="8155b-172">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="8155b-172">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="8155b-173">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="8155b-173">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="8155b-174">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="8155b-174">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="8155b-175">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="8155b-175">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)
