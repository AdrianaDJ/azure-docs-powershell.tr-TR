---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: D23BBF34-80C0-48B1-8E1C-6F345DEC61AD
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/new-Azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/New-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/New-AzWebAppSlot.md
ms.openlocfilehash: 41851c1492c3c14e3129ba04367580b09cf3ffb5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936082"
---
# <span data-ttu-id="2bcd4-101">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2bcd4-101">New-AzWebAppSlot</span></span>

## <span data-ttu-id="2bcd4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2bcd4-102">SYNOPSIS</span></span>
<span data-ttu-id="2bcd4-103">Azure Web App yuvası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2bcd4-103">Creates an Azure Web App slot.</span></span>

## <span data-ttu-id="2bcd4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2bcd4-104">SYNTAX</span></span>

```
New-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [[-AppServicePlan] <String>] [[-SourceWebApp] <Site>] [-IgnoreSourceControl] [-IgnoreCustomHostNames]
 [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2bcd4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2bcd4-105">DESCRIPTION</span></span>
<span data-ttu-id="2bcd4-106">**Yeni-AzWebAppSlot** cmdlet 'i, belirtilen App Service planını ve veri merkezini kullanan bir kaynak grubundaki verili bir Azure Web App yuvası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2bcd4-106">The **New-AzWebAppSlot** cmdlet creates an Azure Web App Slot in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="2bcd4-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2bcd4-107">EXAMPLES</span></span>

### <span data-ttu-id="2bcd4-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2bcd4-108">Example 1</span></span>
```
PS C:\> New-AzWebAppSlot -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -AppServicePlan "ContosoServicePlan" -Slot "Slot001"
```

<span data-ttu-id="2bcd4-109">Bu komut, veri merkezi Batı 'da varsayılan-Web-WestUS adlı var olan kaynak grubundaki Contosositesinin mevcut Web App adları altında Slot001 adlı bir yuva oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2bcd4-109">This command creates a Slot named Slot001 under an existing Web App names ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="2bcd4-110">Bu komut, ContosoServicePlan adında var olan bir App Service planı kullanır.</span><span class="sxs-lookup"><span data-stu-id="2bcd4-110">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="2bcd4-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2bcd4-111">PARAMETERS</span></span>

### <span data-ttu-id="2bcd4-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="2bcd4-112">-AppServicePlan</span></span>
<span data-ttu-id="2bcd4-113">App Service planı adı</span><span class="sxs-lookup"><span data-stu-id="2bcd4-113">App Service Plan Name</span></span>

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

### <span data-ttu-id="2bcd4-114">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="2bcd4-114">-AppSettingsOverrides</span></span>
<span data-ttu-id="2bcd4-115">Uygulama ayarları Hashtable 'ı geçersiz kılıyor</span><span class="sxs-lookup"><span data-stu-id="2bcd4-115">App Settings Overrides Hashtable</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bcd4-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="2bcd4-116">-AseName</span></span>
<span data-ttu-id="2bcd4-117">App Service ortamı adı</span><span class="sxs-lookup"><span data-stu-id="2bcd4-117">App Service Environment Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bcd4-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2bcd4-118">-AseResourceGroupName</span></span>
<span data-ttu-id="2bcd4-119">App Service ortamı kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="2bcd4-119">App Service Environment Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bcd4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bcd4-120">-DefaultProfile</span></span>
<span data-ttu-id="2bcd4-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2bcd4-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2bcd4-122">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="2bcd4-122">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="2bcd4-123">Özel konak adlarını yoksay seçeneği</span><span class="sxs-lookup"><span data-stu-id="2bcd4-123">Ignore Custom HostNames Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bcd4-124">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="2bcd4-124">-IgnoreSourceControl</span></span>
<span data-ttu-id="2bcd4-125">Kaynak denetimi seçeneğini yoksayma</span><span class="sxs-lookup"><span data-stu-id="2bcd4-125">Ignore Source Control Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bcd4-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="2bcd4-126">-Name</span></span>
<span data-ttu-id="2bcd4-127">WEBAPP adı</span><span class="sxs-lookup"><span data-stu-id="2bcd4-127">Webapp Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2bcd4-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2bcd4-128">-ResourceGroupName</span></span>
<span data-ttu-id="2bcd4-129">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="2bcd4-129">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bcd4-130">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="2bcd4-130">-Slot</span></span>
<span data-ttu-id="2bcd4-131">WEBAPP yuva adı</span><span class="sxs-lookup"><span data-stu-id="2bcd4-131">Webapp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bcd4-132">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="2bcd4-132">-SourceWebApp</span></span>
<span data-ttu-id="2bcd4-133">Kaynak WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="2bcd4-133">Source WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2bcd4-134">-Iş</span><span class="sxs-lookup"><span data-stu-id="2bcd4-134">-AsJob</span></span>
<span data-ttu-id="2bcd4-135">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="2bcd4-135">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2bcd4-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bcd4-136">CommonParameters</span></span>
<span data-ttu-id="2bcd4-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2bcd4-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bcd4-138">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2bcd4-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bcd4-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2bcd4-139">INPUTS</span></span>

### <span data-ttu-id="2bcd4-140">Bölge</span><span class="sxs-lookup"><span data-stu-id="2bcd4-140">Site</span></span>
<span data-ttu-id="2bcd4-141">' SourceWebApp ' parametresi ardışık düzenin ' site ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="2bcd4-141">Parameter 'SourceWebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="2bcd4-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2bcd4-142">OUTPUTS</span></span>

## <span data-ttu-id="2bcd4-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2bcd4-143">NOTES</span></span>

## <span data-ttu-id="2bcd4-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2bcd4-144">RELATED LINKS</span></span>

[<span data-ttu-id="2bcd4-145">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2bcd4-145">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="2bcd4-146">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2bcd4-146">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="2bcd4-147">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2bcd4-147">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="2bcd4-148">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2bcd4-148">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="2bcd4-149">Başlangıç-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2bcd4-149">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="2bcd4-150">Dur-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2bcd4-150">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="2bcd4-151">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="2bcd4-151">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="2bcd4-152">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="2bcd4-152">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
