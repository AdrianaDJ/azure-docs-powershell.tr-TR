---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: D23BBF34-80C0-48B1-8E1C-6F345DEC61AD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermwebappslot
schema: 2.0.0
ms.openlocfilehash: f41149c6abb946340acc06b847c72dcabcee18fe
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939206"
---
# <span data-ttu-id="f2e83-101">New-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f2e83-101">New-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="f2e83-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2e83-102">SYNOPSIS</span></span>
<span data-ttu-id="f2e83-103">Azure Web App yuvası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f2e83-103">Creates an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2e83-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f2e83-104">SYNTAX</span></span>

```
New-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [[-AppServicePlan] <String>] [[-SourceWebApp] <Site>] [-IgnoreSourceControl] [-IgnoreCustomHostNames]
 [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2e83-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f2e83-105">DESCRIPTION</span></span>
<span data-ttu-id="f2e83-106">**Yeni-AzureRmWebAppSlot** cmdlet 'i, belirtilen App Service planını ve veri merkezini kullanan bir kaynak grubundaki verili bir Azure Web App yuvası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f2e83-106">The **New-AzureRmWebAppSlot** cmdlet creates an Azure Web App Slot in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="f2e83-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f2e83-107">EXAMPLES</span></span>

### <span data-ttu-id="f2e83-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f2e83-108">Example 1</span></span>
```
PS C:\> New-AzureRmWebAppSlot -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -AppServicePlan "ContosoServicePlan" -Slot "Slot001"
```

<span data-ttu-id="f2e83-109">Bu komut, veri merkezi Batı 'da varsayılan-Web-WestUS adlı var olan kaynak grubundaki Contosositesinin mevcut Web App adları altında Slot001 adlı bir yuva oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f2e83-109">This command creates a Slot named Slot001 under an existing Web App names ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="f2e83-110">Bu komut, ContosoServicePlan adında var olan bir App Service planı kullanır.</span><span class="sxs-lookup"><span data-stu-id="f2e83-110">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="f2e83-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f2e83-111">PARAMETERS</span></span>

### <span data-ttu-id="f2e83-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="f2e83-112">-AppServicePlan</span></span>
<span data-ttu-id="f2e83-113">App Service planı adı</span><span class="sxs-lookup"><span data-stu-id="f2e83-113">App Service Plan Name</span></span>

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

### <span data-ttu-id="f2e83-114">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="f2e83-114">-AppSettingsOverrides</span></span>
<span data-ttu-id="f2e83-115">Uygulama ayarları Hashtable 'ı geçersiz kılıyor</span><span class="sxs-lookup"><span data-stu-id="f2e83-115">App Settings Overrides Hashtable</span></span>

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

### <span data-ttu-id="f2e83-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="f2e83-116">-AseName</span></span>
<span data-ttu-id="f2e83-117">App Service ortamı adı</span><span class="sxs-lookup"><span data-stu-id="f2e83-117">App Service Environment Name</span></span>

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

### <span data-ttu-id="f2e83-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2e83-118">-AseResourceGroupName</span></span>
<span data-ttu-id="f2e83-119">App Service ortamı kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="f2e83-119">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="f2e83-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2e83-120">-DefaultProfile</span></span>
<span data-ttu-id="f2e83-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f2e83-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2e83-122">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="f2e83-122">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="f2e83-123">Özel konak adlarını yoksay seçeneği</span><span class="sxs-lookup"><span data-stu-id="f2e83-123">Ignore Custom HostNames Option</span></span>

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

### <span data-ttu-id="f2e83-124">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="f2e83-124">-IgnoreSourceControl</span></span>
<span data-ttu-id="f2e83-125">Kaynak denetimi seçeneğini yoksayma</span><span class="sxs-lookup"><span data-stu-id="f2e83-125">Ignore Source Control Option</span></span>

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

### <span data-ttu-id="f2e83-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="f2e83-126">-Name</span></span>
<span data-ttu-id="f2e83-127">WEBAPP adı</span><span class="sxs-lookup"><span data-stu-id="f2e83-127">Webapp Name</span></span>

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

### <span data-ttu-id="f2e83-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2e83-128">-ResourceGroupName</span></span>
<span data-ttu-id="f2e83-129">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="f2e83-129">Resource Group Name</span></span>

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

### <span data-ttu-id="f2e83-130">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="f2e83-130">-Slot</span></span>
<span data-ttu-id="f2e83-131">WEBAPP yuva adı</span><span class="sxs-lookup"><span data-stu-id="f2e83-131">Webapp Slot Name</span></span>

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

### <span data-ttu-id="f2e83-132">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="f2e83-132">-SourceWebApp</span></span>
<span data-ttu-id="f2e83-133">Kaynak WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="f2e83-133">Source WebApp Object</span></span>

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

### <span data-ttu-id="f2e83-134">-Iş</span><span class="sxs-lookup"><span data-stu-id="f2e83-134">-AsJob</span></span>
<span data-ttu-id="f2e83-135">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="f2e83-135">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f2e83-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2e83-136">CommonParameters</span></span>
<span data-ttu-id="f2e83-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f2e83-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2e83-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2e83-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2e83-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f2e83-139">INPUTS</span></span>

### <span data-ttu-id="f2e83-140">Bölge</span><span class="sxs-lookup"><span data-stu-id="f2e83-140">Site</span></span>
<span data-ttu-id="f2e83-141">' SourceWebApp ' parametresi ardışık düzenin ' site ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="f2e83-141">Parameter 'SourceWebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="f2e83-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f2e83-142">OUTPUTS</span></span>

## <span data-ttu-id="f2e83-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f2e83-143">NOTES</span></span>

## <span data-ttu-id="f2e83-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f2e83-144">RELATED LINKS</span></span>

[<span data-ttu-id="f2e83-145">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f2e83-145">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="f2e83-146">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f2e83-146">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="f2e83-147">Restart-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f2e83-147">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="f2e83-148">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f2e83-148">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="f2e83-149">Başlangıç-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f2e83-149">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="f2e83-150">Dur-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f2e83-150">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="f2e83-151">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="f2e83-151">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="f2e83-152">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="f2e83-152">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
