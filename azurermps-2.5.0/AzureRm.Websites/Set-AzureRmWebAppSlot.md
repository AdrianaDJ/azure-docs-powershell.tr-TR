---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: FA868206-D8B0-4868-A1D1-D3F96BF3ADCC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/set-azurermwebappslot
schema: 2.0.0
ms.openlocfilehash: 245ce5ab011f03b8d8331b5d80fa4eeb01e19e15
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939814"
---
# <span data-ttu-id="cbfd3-101">Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="cbfd3-101">Set-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="cbfd3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cbfd3-102">SYNOPSIS</span></span>
<span data-ttu-id="cbfd3-103">Azure Web App yuvasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="cbfd3-103">Modifies an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cbfd3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cbfd3-104">SYNTAX</span></span>

### <span data-ttu-id="cbfd3-105">S1</span><span class="sxs-lookup"><span data-stu-id="cbfd3-105">S1</span></span>
```
Set-AzureRmWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-ResourceGroupName] <String> [-Name] <String>
 [[-AssignIdentity] <Boolean>] [[HttpsOnly] <Boolean>] [-Slot] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cbfd3-106">S2</span><span class="sxs-lookup"><span data-stu-id="cbfd3-106">S2</span></span>
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

## <span data-ttu-id="cbfd3-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="cbfd3-107">DESCRIPTION</span></span>
<span data-ttu-id="cbfd3-108">**Set-AzureRmWebApp** cmdlet 'ı bir Azure Web App yuvası ayarlar.</span><span class="sxs-lookup"><span data-stu-id="cbfd3-108">The **Set-AzureRmWebApp** cmdlet sets an Azure Web App Slot.</span></span>

## <span data-ttu-id="cbfd3-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cbfd3-109">EXAMPLES</span></span>

### <span data-ttu-id="cbfd3-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="cbfd3-110">Example 1</span></span>
```
PS C:\> Set-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -HttpLoggingEnabled $true
```

<span data-ttu-id="cbfd3-111">Bu komut, varsayılan-Web-WestUS kaynak grubuyla ilişkilendirilmiş Web App ContosoWebApp ile ilgili Slot001 yuva</span><span class="sxs-lookup"><span data-stu-id="cbfd3-111">This command sets HttpLoggingEnabled to true for Slot Slot001 pertaining to Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="cbfd3-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cbfd3-112">PARAMETERS</span></span>

### <span data-ttu-id="cbfd3-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="cbfd3-113">-AppServicePlan</span></span>
<span data-ttu-id="cbfd3-114">App Service planı adı</span><span class="sxs-lookup"><span data-stu-id="cbfd3-114">App Service Plan Name</span></span>

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

### <span data-ttu-id="cbfd3-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="cbfd3-115">-AppSettings</span></span>
<span data-ttu-id="cbfd3-116">Uygulama ayarları HashTable</span><span class="sxs-lookup"><span data-stu-id="cbfd3-116">App Settings HashTable</span></span>

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

### <span data-ttu-id="cbfd3-117">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="cbfd3-117">-AutoSwapSlotName</span></span>
<span data-ttu-id="cbfd3-118">Otomatik takas için hedef yuva adı</span><span class="sxs-lookup"><span data-stu-id="cbfd3-118">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="cbfd3-119">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="cbfd3-119">-ConnectionStrings</span></span>
<span data-ttu-id="cbfd3-120">Bağlantı dizeleri HashTable</span><span class="sxs-lookup"><span data-stu-id="cbfd3-120">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="cbfd3-121">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="cbfd3-121">-DefaultDocuments</span></span>
<span data-ttu-id="cbfd3-122">Varsayılan belgeler dize dizisi</span><span class="sxs-lookup"><span data-stu-id="cbfd3-122">Default Documents String Array</span></span>

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

### <span data-ttu-id="cbfd3-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbfd3-123">-DefaultProfile</span></span>
<span data-ttu-id="cbfd3-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cbfd3-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cbfd3-125">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="cbfd3-125">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="cbfd3-126">Ayrıntılı hata günlüğü etkin Boole</span><span class="sxs-lookup"><span data-stu-id="cbfd3-126">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="cbfd3-127">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="cbfd3-127">-HandlerMappings</span></span>
<span data-ttu-id="cbfd3-128">İşleyici eşlemeleri IList</span><span class="sxs-lookup"><span data-stu-id="cbfd3-128">Handler Mappings IList</span></span>

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

### <span data-ttu-id="cbfd3-129">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="cbfd3-129">-HttpLoggingEnabled</span></span>
<span data-ttu-id="cbfd3-130">HttpLoggingEnabled Boolean</span><span class="sxs-lookup"><span data-stu-id="cbfd3-130">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="cbfd3-131">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="cbfd3-131">-ManagedPipelineMode</span></span>
<span data-ttu-id="cbfd3-132">Yönetilen ardışık düzen modu adı</span><span class="sxs-lookup"><span data-stu-id="cbfd3-132">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="cbfd3-133">-Ad</span><span class="sxs-lookup"><span data-stu-id="cbfd3-133">-Name</span></span>
<span data-ttu-id="cbfd3-134">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="cbfd3-134">WebApp Name</span></span>

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

### <span data-ttu-id="cbfd3-135">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="cbfd3-135">-NetFrameworkVersion</span></span>
<span data-ttu-id="cbfd3-136">NET Framework sürümü</span><span class="sxs-lookup"><span data-stu-id="cbfd3-136">Net Framework Version</span></span>

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

### <span data-ttu-id="cbfd3-137">-Işçilere</span><span class="sxs-lookup"><span data-stu-id="cbfd3-137">-NumberOfWorkers</span></span>
<span data-ttu-id="cbfd3-138">Tahsis edilecek çalışan sayısı</span><span class="sxs-lookup"><span data-stu-id="cbfd3-138">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="cbfd3-139">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="cbfd3-139">-PhpVersion</span></span>
<span data-ttu-id="cbfd3-140">PHP sürümü</span><span class="sxs-lookup"><span data-stu-id="cbfd3-140">Php Version</span></span>

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

### <span data-ttu-id="cbfd3-141">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="cbfd3-141">-RequestTracingEnabled</span></span>
<span data-ttu-id="cbfd3-142">İstek Izleme etkin Boole değeri</span><span class="sxs-lookup"><span data-stu-id="cbfd3-142">Request Tracing Enabled Boolean</span></span>

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

### <span data-ttu-id="cbfd3-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbfd3-143">-ResourceGroupName</span></span>
<span data-ttu-id="cbfd3-144">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="cbfd3-144">Resource Group Name</span></span>

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

### <span data-ttu-id="cbfd3-145">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="cbfd3-145">-Slot</span></span>
<span data-ttu-id="cbfd3-146">WebApp yuva adı</span><span class="sxs-lookup"><span data-stu-id="cbfd3-146">WebApp Slot Name</span></span>

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

### <span data-ttu-id="cbfd3-147">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="cbfd3-147">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="cbfd3-148">32 bit çalışan süreci Boole kullanma</span><span class="sxs-lookup"><span data-stu-id="cbfd3-148">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="cbfd3-149">-WebApp</span><span class="sxs-lookup"><span data-stu-id="cbfd3-149">-WebApp</span></span>
<span data-ttu-id="cbfd3-150">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="cbfd3-150">WebApp Object</span></span>

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

### <span data-ttu-id="cbfd3-151">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="cbfd3-151">-WebSocketsEnabled</span></span>
<span data-ttu-id="cbfd3-152">Web soketleri etkin Boole değeri</span><span class="sxs-lookup"><span data-stu-id="cbfd3-152">Web Sockets Enabled Boolean</span></span>

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
### <span data-ttu-id="cbfd3-153">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="cbfd3-153">-HttpsOnly</span></span>
<span data-ttu-id="cbfd3-154">Var olan bir yuvada tüm trafiği HTTPS 'ye yönlendirmeyi etkinleştirme/devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="cbfd3-154">Enable/disable redirecting all traffic to HTTPS on an existing slot</span></span>

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
### <span data-ttu-id="cbfd3-155">-Atama kimliği</span><span class="sxs-lookup"><span data-stu-id="cbfd3-155">-AssignIdentity</span></span>
<span data-ttu-id="cbfd3-156">Var olan yuvada MSI 'yi etkinleştirme/devre dışı bırakma [ÖNIZLEME]</span><span class="sxs-lookup"><span data-stu-id="cbfd3-156">Enable/disable MSI on an existing slot [PREVIEW]</span></span>

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

### <span data-ttu-id="cbfd3-157">-Iş</span><span class="sxs-lookup"><span data-stu-id="cbfd3-157">-AsJob</span></span>
<span data-ttu-id="cbfd3-158">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="cbfd3-158">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cbfd3-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbfd3-159">CommonParameters</span></span>
<span data-ttu-id="cbfd3-160">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cbfd3-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbfd3-161">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbfd3-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbfd3-162">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cbfd3-162">INPUTS</span></span>

### <span data-ttu-id="cbfd3-163">32</span><span class="sxs-lookup"><span data-stu-id="cbfd3-163">Int32</span></span>
<span data-ttu-id="cbfd3-164">' Işçilerin ' parametresi ardışık düzenin ' Int32 ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="cbfd3-164">Parameter 'NumberOfWorkers' accepts value of type 'Int32' from the pipeline</span></span>

### <span data-ttu-id="cbfd3-165">Bölge</span><span class="sxs-lookup"><span data-stu-id="cbfd3-165">Site</span></span>
<span data-ttu-id="cbfd3-166">' WebApp ' parametresi ardışık düzenin ' site ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="cbfd3-166">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="cbfd3-167">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cbfd3-167">OUTPUTS</span></span>

## <span data-ttu-id="cbfd3-168">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cbfd3-168">NOTES</span></span>

## <span data-ttu-id="cbfd3-169">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cbfd3-169">RELATED LINKS</span></span>

[<span data-ttu-id="cbfd3-170">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="cbfd3-170">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="cbfd3-171">Yeni-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="cbfd3-171">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="cbfd3-172">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="cbfd3-172">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="cbfd3-173">Restart-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="cbfd3-173">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="cbfd3-174">Başlangıç-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="cbfd3-174">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="cbfd3-175">Dur-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="cbfd3-175">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="cbfd3-176">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="cbfd3-176">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)
