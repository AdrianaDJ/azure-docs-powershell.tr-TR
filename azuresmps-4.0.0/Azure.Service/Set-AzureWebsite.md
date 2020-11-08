---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 9D821623-DEF9-49E4-9C44-10643A92A2E7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7f6690aa45125a0d1b3383b08443234f47a1f7e3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105433"
---
# <span data-ttu-id="08565-101">Set-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="08565-101">Set-AzureWebsite</span></span>

## <span data-ttu-id="08565-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="08565-102">SYNOPSIS</span></span>
<span data-ttu-id="08565-103">Azure 'da çalışan bir Web sitesini yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="08565-103">Configures a website running in Azure.</span></span>

## <span data-ttu-id="08565-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="08565-104">SYNTAX</span></span>

```
Set-AzureWebsite [-NumberOfWorkers <Int32>] [-DefaultDocuments <String[]>] [-NetFrameworkVersion <String>]
 [-PhpVersion <String>] [-RequestTracingEnabled <Boolean>] [-HttpLoggingEnabled <Boolean>]
 [-DetailedErrorLoggingEnabled <Boolean>] [-HostNames <String[]>] [-AppSettings <Hashtable>]
 [-Metadata <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.NameValuePair]>]
 [-ConnectionStrings <ConnStringPropertyBag>] [-HandlerMappings <HandlerMapping[]>]
 [-SiteWithConfig <SiteWithConfig>] [-PassThru] [-ManagedPipelineMode <ManagedPipelineMode>]
 [-WebSocketsEnabled <Boolean>]
 [-RoutingRules <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.RoutingRule]>]
 [-Use32BitWorkerProcess <Boolean>] [-AutoSwapSlotName <String>]
 [-SlotStickyAppSettingNames <System.Collections.Generic.List`1[System.String]>]
 [-SlotStickyConnectionStringNames <System.Collections.Generic.List`1[System.String]>] [-Name <String>]
 [-Slot <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="08565-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="08565-105">DESCRIPTION</span></span>
<span data-ttu-id="08565-106">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="08565-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="08565-107">Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="08565-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="08565-108">**Set-AzureWebsite** cmdlet 'ı, Azure 'da çalışan bir Web sitesini yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="08565-108">The **Set-AzureWebsite** cmdlet configures a website running in Azure.</span></span>

## <span data-ttu-id="08565-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="08565-109">EXAMPLES</span></span>

### <span data-ttu-id="08565-110">Örnek 1: Web sitesi için HTTP günlüğünü etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="08565-110">Example 1: Enable HTTP logging for a website</span></span>
```
PS C:\> Set-AzureWebsite -HttpLoggingEnabled 1
```

<span data-ttu-id="08565-111">Bu örnekte HTTP günlüğe kaydetme etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="08565-111">This example enables HTTP logging.</span></span>

### <span data-ttu-id="08565-112">Örnek 2: Web sitesi için depolama bilgilerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="08565-112">Example 2: Set storage credentials for a website</span></span>
```
PS C:\> $settings = New-Object Hashtable$settings["AZURE_STORAGE_ACCOUNT"= myaccountname$settings["AZURE_STORAGE_ACCESS_KEY"] = myaccesskeySet-AzureWebsite -AppSettings $settings myWebsite
```

<span data-ttu-id="08565-113">Bu örnekte, AZURE_STORAGE_ACCOUNT ve AZURE_STORAGE_ACCESS_KEY için ortam değişkenleriyle birlikte myWebsite adlı Web sitesindeki depolama bilgileri ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="08565-113">This example sets storage credentials in a website named myWebsite with environment variables for AZURE_STORAGE_ACCOUNT and AZURE_STORAGE_ACCESS_KEY.</span></span>

## <span data-ttu-id="08565-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="08565-114">PARAMETERS</span></span>

### <span data-ttu-id="08565-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="08565-115">-AppSettings</span></span>
<span data-ttu-id="08565-116">Web sitesi tarafından kullanılacak ortam değişkenlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="08565-116">Specifies the environment variables that will be used by the website.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08565-117">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="08565-117">-AutoSwapSlotName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08565-118">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="08565-118">-ConnectionStrings</span></span>
<span data-ttu-id="08565-119">Web sitesi tarafından kullanılan bağlantı dizelerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="08565-119">Specifies the connection strings used by the website.</span></span>

```yaml
Type: ConnStringPropertyBag
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08565-120">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="08565-120">-DefaultDocuments</span></span>
<span data-ttu-id="08565-121">Web sitesine gözatarken otomatik olarak görüntülenen belgeleri belirtir.</span><span class="sxs-lookup"><span data-stu-id="08565-121">Specifies the documents that are automatically displayed when browsing the website.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08565-122">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="08565-122">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="08565-123">Web sitesi için ayrıntılı IIS hatalarının günlüğe kaydedilip kaydedilmeyeceğini belirler.</span><span class="sxs-lookup"><span data-stu-id="08565-123">Determines whether detailed IIS errors are logged for the website.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08565-124">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="08565-124">-HandlerMappings</span></span>
<span data-ttu-id="08565-125">Web sitesi tarafından kullanılan İşleyici eşlemelerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="08565-125">Specifies the handler mappings used by the website.</span></span>

```yaml
Type: HandlerMapping[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08565-126">-Ana makine adları</span><span class="sxs-lookup"><span data-stu-id="08565-126">-HostNames</span></span>
<span data-ttu-id="08565-127">Web sitesine erişmek için kullanılabilecek tam nitelikli ana bilgisayar adlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="08565-127">Specifies the fully qualified host names that can be used to access the website.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08565-128">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="08565-128">-HttpLoggingEnabled</span></span>
<span data-ttu-id="08565-129">Web sitesi için http günlüğünün etkinleştirilip etkinleştirilmediğini belirler.</span><span class="sxs-lookup"><span data-stu-id="08565-129">Determines whether http logging is enabled for the website.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08565-130">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="08565-130">-ManagedPipelineMode</span></span>
<span data-ttu-id="08565-131">Yönetilen ardışık düzen modunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="08565-131">Specifies the managed pipeline mode.</span></span>

```yaml
Type: ManagedPipelineMode
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08565-132">-Metadata</span><span class="sxs-lookup"><span data-stu-id="08565-132">-Metadata</span></span>
<span data-ttu-id="08565-133">Web sitesi için meta verileri belirtir.</span><span class="sxs-lookup"><span data-stu-id="08565-133">Specifies the metadata for the website.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.NameValuePair]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08565-134">-Ad</span><span class="sxs-lookup"><span data-stu-id="08565-134">-Name</span></span>
<span data-ttu-id="08565-135">Web sitesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="08565-135">Specifies the name of the website.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08565-136">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="08565-136">-NetFrameworkVersion</span></span>
<span data-ttu-id="08565-137">Web sitesi için gereken .NET Framework sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="08565-137">Specifies the version of the .Net Framework required by the website.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08565-138">-Işçilere</span><span class="sxs-lookup"><span data-stu-id="08565-138">-NumberOfWorkers</span></span>
<span data-ttu-id="08565-139">Web sitesini çalıştıran çalışan işlemlerinin sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="08565-139">Specifies the number of worker processes running the website.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08565-140">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="08565-140">-PassThru</span></span>
<span data-ttu-id="08565-141">Bu cmdlet 'in **Boole** değeri döndürdüğü anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="08565-141">Indicates that this cmdlet returns a **Boolean** value.</span></span>

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

### <span data-ttu-id="08565-142">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="08565-142">-PhpVersion</span></span>
<span data-ttu-id="08565-143">Web sitesi için gereken PHP sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="08565-143">Specifies the PHP version required by the website.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08565-144">-Profil</span><span class="sxs-lookup"><span data-stu-id="08565-144">-Profile</span></span>
<span data-ttu-id="08565-145">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="08565-145">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="08565-146">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="08565-146">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08565-147">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="08565-147">-RequestTracingEnabled</span></span>
<span data-ttu-id="08565-148">Web sitesi için istek izlemenin etkinleştirilip etkinleştirilmediğini belirler.</span><span class="sxs-lookup"><span data-stu-id="08565-148">Determines whether request tracing is enabled for the website.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08565-149">-RoutingRules</span><span class="sxs-lookup"><span data-stu-id="08565-149">-RoutingRules</span></span>
<span data-ttu-id="08565-150">Üretimde test için kullanılacak yönlendirme kurallarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="08565-150">Specifies the routing rules to use for testing in production.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.RoutingRule]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08565-151">-SiteWithConfig</span><span class="sxs-lookup"><span data-stu-id="08565-151">-SiteWithConfig</span></span>
<span data-ttu-id="08565-152">Web sitesi tarafından kullanılan yapılandırmayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="08565-152">Specifies the configuration used by the website.</span></span>

```yaml
Type: SiteWithConfig
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08565-153">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="08565-153">-Slot</span></span>
<span data-ttu-id="08565-154">Web sitesinin yuva adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="08565-154">Specifies the slot name of the website.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08565-155">-SlotStickyAppSettingNames</span><span class="sxs-lookup"><span data-stu-id="08565-155">-SlotStickyAppSettingNames</span></span>
```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08565-156">-SlotStickyConnectionStringNames</span><span class="sxs-lookup"><span data-stu-id="08565-156">-SlotStickyConnectionStringNames</span></span>
```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08565-157">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="08565-157">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="08565-158">32 bit modunun etkinleştirilip etkinleştirilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="08565-158">Specifies whether to enable 32-bit mode.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08565-159">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="08565-159">-WebSocketsEnabled</span></span>
<span data-ttu-id="08565-160">WebSockets etkinleştirilip etkinleştirilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="08565-160">Specifies whether to enable WebSockets.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08565-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08565-161">CommonParameters</span></span>
<span data-ttu-id="08565-162">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="08565-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08565-163">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08565-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08565-164">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="08565-164">INPUTS</span></span>

## <span data-ttu-id="08565-165">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="08565-165">OUTPUTS</span></span>

## <span data-ttu-id="08565-166">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="08565-166">NOTES</span></span>

## <span data-ttu-id="08565-167">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="08565-167">RELATED LINKS</span></span>

[<span data-ttu-id="08565-168">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="08565-168">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="08565-169">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="08565-169">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="08565-170">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="08565-170">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)


