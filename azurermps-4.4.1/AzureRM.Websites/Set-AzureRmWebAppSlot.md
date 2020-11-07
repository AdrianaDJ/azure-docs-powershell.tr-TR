---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: FA868206-D8B0-4868-A1D1-D3F96BF3ADCC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebAppSlot.md
ms.openlocfilehash: 4780deac3d335060d5a3d7e262a61184b2e0c3b4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762048"
---
# <span data-ttu-id="49267-101">Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="49267-101">Set-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="49267-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49267-102">SYNOPSIS</span></span>
<span data-ttu-id="49267-103">Azure Web App yuvasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="49267-103">Modifies an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="49267-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="49267-104">SYNTAX</span></span>

### <span data-ttu-id="49267-105">S1</span><span class="sxs-lookup"><span data-stu-id="49267-105">S1</span></span>
```
Set-AzureRmWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-ResourceGroupName] <String> [-Name] <String>
 [-Slot] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="49267-106">S2</span><span class="sxs-lookup"><span data-stu-id="49267-106">S2</span></span>
```
Set-AzureRmWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49267-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="49267-107">DESCRIPTION</span></span>
<span data-ttu-id="49267-108">**Set-AzureRmWebApp** cmdlet 'ı bir Azure Web App yuvası ayarlar.</span><span class="sxs-lookup"><span data-stu-id="49267-108">The **Set-AzureRmWebApp** cmdlet sets an Azure Web App Slot.</span></span>

## <span data-ttu-id="49267-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="49267-109">EXAMPLES</span></span>

### <span data-ttu-id="49267-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="49267-110">Example 1</span></span>
```
PS C:\> Set-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -HttpLoggingEnabled $true
```

<span data-ttu-id="49267-111">Bu komut, varsayılan-Web-WestUS kaynak grubuyla ilişkilendirilmiş Web App ContosoWebApp ile ilgili Slot001 yuva</span><span class="sxs-lookup"><span data-stu-id="49267-111">This command sets HttpLoggingEnabled to true for Slot Slot001 pertaining to Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="49267-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="49267-112">PARAMETERS</span></span>

### <span data-ttu-id="49267-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="49267-113">-AppServicePlan</span></span>
<span data-ttu-id="49267-114">App Service planı adı</span><span class="sxs-lookup"><span data-stu-id="49267-114">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49267-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="49267-115">-AppSettings</span></span>
<span data-ttu-id="49267-116">Uygulama ayarları HashTable</span><span class="sxs-lookup"><span data-stu-id="49267-116">App Settings HashTable</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49267-117">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="49267-117">-AutoSwapSlotName</span></span>
<span data-ttu-id="49267-118">Otomatik takas için hedef yuva adı</span><span class="sxs-lookup"><span data-stu-id="49267-118">Destination slot name for auto swap</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49267-119">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="49267-119">-ConnectionStrings</span></span>
<span data-ttu-id="49267-120">Bağlantı dizeleri HashTable</span><span class="sxs-lookup"><span data-stu-id="49267-120">Connection Strings HashTable</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49267-121">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="49267-121">-DefaultDocuments</span></span>
<span data-ttu-id="49267-122">Varsayılan belgeler dize dizisi</span><span class="sxs-lookup"><span data-stu-id="49267-122">Default Documents String Array</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49267-123">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="49267-123">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="49267-124">Ayrıntılı hata günlüğü etkin Boole</span><span class="sxs-lookup"><span data-stu-id="49267-124">Detailed Error Logging Enabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49267-125">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="49267-125">-HandlerMappings</span></span>
<span data-ttu-id="49267-126">İşleyici eşlemeleri IList</span><span class="sxs-lookup"><span data-stu-id="49267-126">Handler Mappings IList</span></span>

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

### <span data-ttu-id="49267-127">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="49267-127">-HttpLoggingEnabled</span></span>
<span data-ttu-id="49267-128">HttpLoggingEnabled Boolean</span><span class="sxs-lookup"><span data-stu-id="49267-128">HttpLoggingEnabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49267-129">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="49267-129">-ManagedPipelineMode</span></span>
<span data-ttu-id="49267-130">Yönetilen ardışık düzen modu adı</span><span class="sxs-lookup"><span data-stu-id="49267-130">Managed Pipeline Mode Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Classic, Integrated

Required: False
Position: 13
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49267-131">-Ad</span><span class="sxs-lookup"><span data-stu-id="49267-131">-Name</span></span>
<span data-ttu-id="49267-132">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="49267-132">WebApp Name</span></span>

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

### <span data-ttu-id="49267-133">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="49267-133">-NetFrameworkVersion</span></span>
<span data-ttu-id="49267-134">NET Framework sürümü</span><span class="sxs-lookup"><span data-stu-id="49267-134">Net Framework Version</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49267-135">-Işçilere</span><span class="sxs-lookup"><span data-stu-id="49267-135">-NumberOfWorkers</span></span>
<span data-ttu-id="49267-136">Tahsis edilecek çalışan sayısı</span><span class="sxs-lookup"><span data-stu-id="49267-136">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="49267-137">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="49267-137">-PhpVersion</span></span>
<span data-ttu-id="49267-138">PHP sürümü</span><span class="sxs-lookup"><span data-stu-id="49267-138">Php Version</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49267-139">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="49267-139">-RequestTracingEnabled</span></span>
<span data-ttu-id="49267-140">İstek Izleme etkin Boole değeri</span><span class="sxs-lookup"><span data-stu-id="49267-140">Request Tracing Enabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49267-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49267-141">-ResourceGroupName</span></span>
<span data-ttu-id="49267-142">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="49267-142">Resource Group Name</span></span>

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

### <span data-ttu-id="49267-143">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="49267-143">-Slot</span></span>
<span data-ttu-id="49267-144">WebApp yuva adı</span><span class="sxs-lookup"><span data-stu-id="49267-144">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49267-145">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="49267-145">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="49267-146">32 bit çalışan süreci Boole kullanma</span><span class="sxs-lookup"><span data-stu-id="49267-146">Use 32-bit Worker Process Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 15
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49267-147">-WebApp</span><span class="sxs-lookup"><span data-stu-id="49267-147">-WebApp</span></span>
<span data-ttu-id="49267-148">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="49267-148">WebApp Object</span></span>

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

### <span data-ttu-id="49267-149">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="49267-149">-WebSocketsEnabled</span></span>
<span data-ttu-id="49267-150">Web soketleri etkin Boole değeri</span><span class="sxs-lookup"><span data-stu-id="49267-150">Web Sockets Enabled Boolean</span></span>

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

### <span data-ttu-id="49267-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49267-151">-DefaultProfile</span></span>
<span data-ttu-id="49267-152">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="49267-152">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49267-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49267-153">CommonParameters</span></span>
<span data-ttu-id="49267-154">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="49267-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49267-155">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49267-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49267-156">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="49267-156">INPUTS</span></span>

### <span data-ttu-id="49267-157">32</span><span class="sxs-lookup"><span data-stu-id="49267-157">Int32</span></span>
<span data-ttu-id="49267-158">' Işçilerin ' parametresi ardışık düzenin ' Int32 ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="49267-158">Parameter 'NumberOfWorkers' accepts value of type 'Int32' from the pipeline</span></span>

### <span data-ttu-id="49267-159">Bölge</span><span class="sxs-lookup"><span data-stu-id="49267-159">Site</span></span>
<span data-ttu-id="49267-160">' WebApp ' parametresi ardışık düzenin ' site ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="49267-160">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="49267-161">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="49267-161">OUTPUTS</span></span>

## <span data-ttu-id="49267-162">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="49267-162">NOTES</span></span>

## <span data-ttu-id="49267-163">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="49267-163">RELATED LINKS</span></span>

[<span data-ttu-id="49267-164">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="49267-164">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="49267-165">Yeni-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="49267-165">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="49267-166">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="49267-166">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="49267-167">Restart-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="49267-167">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="49267-168">Başlangıç-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="49267-168">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="49267-169">Dur-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="49267-169">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="49267-170">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="49267-170">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)
