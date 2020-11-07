---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: FA868206-D8B0-4868-A1D1-D3F96BF3ADCC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/set-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebAppSlot.md
ms.openlocfilehash: 717f355326acc4d169bee1e93d98446fa052a5e1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763934"
---
# <span data-ttu-id="ac128-101">Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ac128-101">Set-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="ac128-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac128-102">SYNOPSIS</span></span>
<span data-ttu-id="ac128-103">Azure Web App yuvasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="ac128-103">Modifies an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ac128-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ac128-104">SYNTAX</span></span>

### <span data-ttu-id="ac128-105">S1</span><span class="sxs-lookup"><span data-stu-id="ac128-105">S1</span></span>
```
Set-AzureRmWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-ResourceGroupName] <String> [-Name] <String>
 [-Slot] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ac128-106">S2</span><span class="sxs-lookup"><span data-stu-id="ac128-106">S2</span></span>
```
Set-AzureRmWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-WebApp] <Site> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac128-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="ac128-107">DESCRIPTION</span></span>
<span data-ttu-id="ac128-108">**Set-AzureRmWebApp** cmdlet 'ı bir Azure Web App yuvası ayarlar.</span><span class="sxs-lookup"><span data-stu-id="ac128-108">The **Set-AzureRmWebApp** cmdlet sets an Azure Web App Slot.</span></span>

## <span data-ttu-id="ac128-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ac128-109">EXAMPLES</span></span>

### <span data-ttu-id="ac128-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ac128-110">Example 1</span></span>
```
PS C:\> Set-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -HttpLoggingEnabled $true
```

<span data-ttu-id="ac128-111">Bu komut, varsayılan-Web-WestUS kaynak grubuyla ilişkilendirilmiş Web App ContosoWebApp ile ilgili Slot001 yuva</span><span class="sxs-lookup"><span data-stu-id="ac128-111">This command sets HttpLoggingEnabled to true for Slot Slot001 pertaining to Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="ac128-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ac128-112">PARAMETERS</span></span>

### <span data-ttu-id="ac128-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ac128-113">-AppServicePlan</span></span>
<span data-ttu-id="ac128-114">App Service planı adı</span><span class="sxs-lookup"><span data-stu-id="ac128-114">App Service Plan Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac128-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="ac128-115">-AppSettings</span></span>
<span data-ttu-id="ac128-116">Uygulama ayarları HashTable</span><span class="sxs-lookup"><span data-stu-id="ac128-116">App Settings HashTable</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac128-117">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="ac128-117">-AutoSwapSlotName</span></span>
<span data-ttu-id="ac128-118">Otomatik takas için hedef yuva adı</span><span class="sxs-lookup"><span data-stu-id="ac128-118">Destination slot name for auto swap</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac128-119">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="ac128-119">-ConnectionStrings</span></span>
<span data-ttu-id="ac128-120">Bağlantı dizeleri HashTable</span><span class="sxs-lookup"><span data-stu-id="ac128-120">Connection Strings HashTable</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac128-121">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="ac128-121">-DefaultDocuments</span></span>
<span data-ttu-id="ac128-122">Varsayılan belgeler dize dizisi</span><span class="sxs-lookup"><span data-stu-id="ac128-122">Default Documents String Array</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac128-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac128-123">-DefaultProfile</span></span>
<span data-ttu-id="ac128-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ac128-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac128-125">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="ac128-125">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="ac128-126">Ayrıntılı hata günlüğü etkin Boole</span><span class="sxs-lookup"><span data-stu-id="ac128-126">Detailed Error Logging Enabled Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac128-127">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="ac128-127">-HandlerMappings</span></span>
<span data-ttu-id="ac128-128">İşleyici eşlemeleri IList</span><span class="sxs-lookup"><span data-stu-id="ac128-128">Handler Mappings IList</span></span>

```yaml
Type: System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 12
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac128-129">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="ac128-129">-HttpLoggingEnabled</span></span>
<span data-ttu-id="ac128-130">HttpLoggingEnabled Boolean</span><span class="sxs-lookup"><span data-stu-id="ac128-130">HttpLoggingEnabled Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac128-131">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="ac128-131">-ManagedPipelineMode</span></span>
<span data-ttu-id="ac128-132">Yönetilen ardışık düzen modu adı</span><span class="sxs-lookup"><span data-stu-id="ac128-132">Managed Pipeline Mode Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Classic, Integrated

Required: False
Position: 13
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac128-133">-Ad</span><span class="sxs-lookup"><span data-stu-id="ac128-133">-Name</span></span>
<span data-ttu-id="ac128-134">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="ac128-134">WebApp Name</span></span>

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

### <span data-ttu-id="ac128-135">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="ac128-135">-NetFrameworkVersion</span></span>
<span data-ttu-id="ac128-136">NET Framework sürümü</span><span class="sxs-lookup"><span data-stu-id="ac128-136">Net Framework Version</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac128-137">-Işçilere</span><span class="sxs-lookup"><span data-stu-id="ac128-137">-NumberOfWorkers</span></span>
<span data-ttu-id="ac128-138">Tahsis edilecek çalışan sayısı</span><span class="sxs-lookup"><span data-stu-id="ac128-138">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="ac128-139">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="ac128-139">-PhpVersion</span></span>
<span data-ttu-id="ac128-140">PHP sürümü</span><span class="sxs-lookup"><span data-stu-id="ac128-140">Php Version</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac128-141">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="ac128-141">-RequestTracingEnabled</span></span>
<span data-ttu-id="ac128-142">İstek Izleme etkin Boole değeri</span><span class="sxs-lookup"><span data-stu-id="ac128-142">Request Tracing Enabled Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac128-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac128-143">-ResourceGroupName</span></span>
<span data-ttu-id="ac128-144">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="ac128-144">Resource Group Name</span></span>

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

### <span data-ttu-id="ac128-145">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="ac128-145">-Slot</span></span>
<span data-ttu-id="ac128-146">WebApp yuva adı</span><span class="sxs-lookup"><span data-stu-id="ac128-146">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac128-147">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="ac128-147">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="ac128-148">32 bit çalışan süreci Boole kullanma</span><span class="sxs-lookup"><span data-stu-id="ac128-148">Use 32-bit Worker Process Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 15
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac128-149">-WebApp</span><span class="sxs-lookup"><span data-stu-id="ac128-149">-WebApp</span></span>
<span data-ttu-id="ac128-150">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="ac128-150">WebApp Object</span></span>

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

### <span data-ttu-id="ac128-151">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="ac128-151">-WebSocketsEnabled</span></span>
<span data-ttu-id="ac128-152">Web soketleri etkin Boole değeri</span><span class="sxs-lookup"><span data-stu-id="ac128-152">Web Sockets Enabled Boolean</span></span>

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
### <span data-ttu-id="ac128-153">-Iş</span><span class="sxs-lookup"><span data-stu-id="ac128-153">-AsJob</span></span>
<span data-ttu-id="ac128-154">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="ac128-154">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ac128-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac128-155">CommonParameters</span></span>
<span data-ttu-id="ac128-156">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ac128-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac128-157">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac128-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac128-158">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ac128-158">INPUTS</span></span>

### <span data-ttu-id="ac128-159">32</span><span class="sxs-lookup"><span data-stu-id="ac128-159">Int32</span></span>
<span data-ttu-id="ac128-160">' Işçilerin ' parametresi ardışık düzenin ' Int32 ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="ac128-160">Parameter 'NumberOfWorkers' accepts value of type 'Int32' from the pipeline</span></span>

### <span data-ttu-id="ac128-161">Bölge</span><span class="sxs-lookup"><span data-stu-id="ac128-161">Site</span></span>
<span data-ttu-id="ac128-162">' WebApp ' parametresi ardışık düzenin ' site ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="ac128-162">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="ac128-163">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ac128-163">OUTPUTS</span></span>

## <span data-ttu-id="ac128-164">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ac128-164">NOTES</span></span>

## <span data-ttu-id="ac128-165">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ac128-165">RELATED LINKS</span></span>

[<span data-ttu-id="ac128-166">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ac128-166">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="ac128-167">Yeni-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ac128-167">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="ac128-168">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ac128-168">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="ac128-169">Restart-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ac128-169">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="ac128-170">Başlangıç-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ac128-170">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="ac128-171">Dur-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ac128-171">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="ac128-172">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ac128-172">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)
