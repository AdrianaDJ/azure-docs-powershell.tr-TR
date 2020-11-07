---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: FA868206-D8B0-4868-A1D1-D3F96BF3ADCC
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/set-Azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Set-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Set-AzWebAppSlot.md
ms.openlocfilehash: b6cb41e49695fa7fd9fa0efdefdbefb2b23229a5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936061"
---
# <span data-ttu-id="d4963-101">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d4963-101">Set-AzWebAppSlot</span></span>

## <span data-ttu-id="d4963-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4963-102">SYNOPSIS</span></span>
<span data-ttu-id="d4963-103">Azure Web App yuvasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="d4963-103">Modifies an Azure Web App slot.</span></span>

## <span data-ttu-id="d4963-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d4963-104">SYNTAX</span></span>

### <span data-ttu-id="d4963-105">S1</span><span class="sxs-lookup"><span data-stu-id="d4963-105">S1</span></span>
```
Set-AzWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-ResourceGroupName] <String> [-Name] <String>
 [[-AssignIdentity] <Boolean>] [[HttpsOnly] <Boolean>] [-Slot] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d4963-106">S2</span><span class="sxs-lookup"><span data-stu-id="d4963-106">S2</span></span>
```
Set-AzWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-WebApp] <Site> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d4963-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d4963-107">DESCRIPTION</span></span>
<span data-ttu-id="d4963-108">**Set-AzWebApp** cmdlet 'ı bir Azure Web App yuvasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="d4963-108">The **Set-AzWebApp** cmdlet sets an Azure Web App Slot.</span></span>

## <span data-ttu-id="d4963-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d4963-109">EXAMPLES</span></span>

### <span data-ttu-id="d4963-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d4963-110">Example 1</span></span>
```
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -HttpLoggingEnabled $true
```

<span data-ttu-id="d4963-111">Bu komut, varsayılan-Web-WestUS kaynak grubuyla ilişkilendirilmiş Web App ContosoWebApp ile ilgili Slot001 yuva</span><span class="sxs-lookup"><span data-stu-id="d4963-111">This command sets HttpLoggingEnabled to true for Slot Slot001 pertaining to Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="d4963-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d4963-112">PARAMETERS</span></span>

### <span data-ttu-id="d4963-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="d4963-113">-AppServicePlan</span></span>
<span data-ttu-id="d4963-114">App Service planı adı</span><span class="sxs-lookup"><span data-stu-id="d4963-114">App Service Plan Name</span></span>

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

### <span data-ttu-id="d4963-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="d4963-115">-AppSettings</span></span>
<span data-ttu-id="d4963-116">Uygulama ayarları HashTable</span><span class="sxs-lookup"><span data-stu-id="d4963-116">App Settings HashTable</span></span>

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

### <span data-ttu-id="d4963-117">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="d4963-117">-AutoSwapSlotName</span></span>
<span data-ttu-id="d4963-118">Otomatik takas için hedef yuva adı</span><span class="sxs-lookup"><span data-stu-id="d4963-118">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="d4963-119">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="d4963-119">-ConnectionStrings</span></span>
<span data-ttu-id="d4963-120">Bağlantı dizeleri HashTable</span><span class="sxs-lookup"><span data-stu-id="d4963-120">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="d4963-121">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="d4963-121">-DefaultDocuments</span></span>
<span data-ttu-id="d4963-122">Varsayılan belgeler dize dizisi</span><span class="sxs-lookup"><span data-stu-id="d4963-122">Default Documents String Array</span></span>

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

### <span data-ttu-id="d4963-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4963-123">-DefaultProfile</span></span>
<span data-ttu-id="d4963-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d4963-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d4963-125">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="d4963-125">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="d4963-126">Ayrıntılı hata günlüğü etkin Boole</span><span class="sxs-lookup"><span data-stu-id="d4963-126">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="d4963-127">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="d4963-127">-HandlerMappings</span></span>
<span data-ttu-id="d4963-128">İşleyici eşlemeleri IList</span><span class="sxs-lookup"><span data-stu-id="d4963-128">Handler Mappings IList</span></span>

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

### <span data-ttu-id="d4963-129">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="d4963-129">-HttpLoggingEnabled</span></span>
<span data-ttu-id="d4963-130">HttpLoggingEnabled Boolean</span><span class="sxs-lookup"><span data-stu-id="d4963-130">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="d4963-131">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="d4963-131">-ManagedPipelineMode</span></span>
<span data-ttu-id="d4963-132">Yönetilen ardışık düzen modu adı</span><span class="sxs-lookup"><span data-stu-id="d4963-132">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="d4963-133">-Ad</span><span class="sxs-lookup"><span data-stu-id="d4963-133">-Name</span></span>
<span data-ttu-id="d4963-134">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="d4963-134">WebApp Name</span></span>

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

### <span data-ttu-id="d4963-135">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="d4963-135">-NetFrameworkVersion</span></span>
<span data-ttu-id="d4963-136">NET Framework sürümü</span><span class="sxs-lookup"><span data-stu-id="d4963-136">Net Framework Version</span></span>

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

### <span data-ttu-id="d4963-137">-Işçilere</span><span class="sxs-lookup"><span data-stu-id="d4963-137">-NumberOfWorkers</span></span>
<span data-ttu-id="d4963-138">Tahsis edilecek çalışan sayısı</span><span class="sxs-lookup"><span data-stu-id="d4963-138">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="d4963-139">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="d4963-139">-PhpVersion</span></span>
<span data-ttu-id="d4963-140">PHP sürümü</span><span class="sxs-lookup"><span data-stu-id="d4963-140">Php Version</span></span>

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

### <span data-ttu-id="d4963-141">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="d4963-141">-RequestTracingEnabled</span></span>
<span data-ttu-id="d4963-142">İstek Izleme etkin Boole değeri</span><span class="sxs-lookup"><span data-stu-id="d4963-142">Request Tracing Enabled Boolean</span></span>

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

### <span data-ttu-id="d4963-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4963-143">-ResourceGroupName</span></span>
<span data-ttu-id="d4963-144">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="d4963-144">Resource Group Name</span></span>

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

### <span data-ttu-id="d4963-145">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="d4963-145">-Slot</span></span>
<span data-ttu-id="d4963-146">WebApp yuva adı</span><span class="sxs-lookup"><span data-stu-id="d4963-146">WebApp Slot Name</span></span>

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

### <span data-ttu-id="d4963-147">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="d4963-147">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="d4963-148">32 bit çalışan süreci Boole kullanma</span><span class="sxs-lookup"><span data-stu-id="d4963-148">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="d4963-149">-WebApp</span><span class="sxs-lookup"><span data-stu-id="d4963-149">-WebApp</span></span>
<span data-ttu-id="d4963-150">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="d4963-150">WebApp Object</span></span>

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

### <span data-ttu-id="d4963-151">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="d4963-151">-WebSocketsEnabled</span></span>
<span data-ttu-id="d4963-152">Web soketleri etkin Boole değeri</span><span class="sxs-lookup"><span data-stu-id="d4963-152">Web Sockets Enabled Boolean</span></span>

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
### <span data-ttu-id="d4963-153">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="d4963-153">-HttpsOnly</span></span>
<span data-ttu-id="d4963-154">Var olan bir yuvada tüm trafiği HTTPS 'ye yönlendirmeyi etkinleştirme/devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="d4963-154">Enable/disable redirecting all traffic to HTTPS on an existing slot</span></span>

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
### <span data-ttu-id="d4963-155">-Atama kimliği</span><span class="sxs-lookup"><span data-stu-id="d4963-155">-AssignIdentity</span></span>
<span data-ttu-id="d4963-156">Var olan yuvada MSI 'yi etkinleştirme/devre dışı bırakma [ÖNIZLEME]</span><span class="sxs-lookup"><span data-stu-id="d4963-156">Enable/disable MSI on an existing slot [PREVIEW]</span></span>

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

### <span data-ttu-id="d4963-157">-Iş</span><span class="sxs-lookup"><span data-stu-id="d4963-157">-AsJob</span></span>
<span data-ttu-id="d4963-158">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="d4963-158">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d4963-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4963-159">CommonParameters</span></span>
<span data-ttu-id="d4963-160">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d4963-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4963-161">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4963-161">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4963-162">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d4963-162">INPUTS</span></span>

### <span data-ttu-id="d4963-163">32</span><span class="sxs-lookup"><span data-stu-id="d4963-163">Int32</span></span>
<span data-ttu-id="d4963-164">' Işçilerin ' parametresi ardışık düzenin ' Int32 ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="d4963-164">Parameter 'NumberOfWorkers' accepts value of type 'Int32' from the pipeline</span></span>

### <span data-ttu-id="d4963-165">Bölge</span><span class="sxs-lookup"><span data-stu-id="d4963-165">Site</span></span>
<span data-ttu-id="d4963-166">' WebApp ' parametresi ardışık düzenin ' site ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="d4963-166">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="d4963-167">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d4963-167">OUTPUTS</span></span>

## <span data-ttu-id="d4963-168">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d4963-168">NOTES</span></span>

## <span data-ttu-id="d4963-169">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d4963-169">RELATED LINKS</span></span>

[<span data-ttu-id="d4963-170">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d4963-170">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="d4963-171">Yeni-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d4963-171">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="d4963-172">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d4963-172">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="d4963-173">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d4963-173">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="d4963-174">Başlangıç-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d4963-174">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="d4963-175">Dur-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d4963-175">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="d4963-176">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="d4963-176">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)
