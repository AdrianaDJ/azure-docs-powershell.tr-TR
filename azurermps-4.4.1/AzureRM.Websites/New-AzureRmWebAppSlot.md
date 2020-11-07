---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: D23BBF34-80C0-48B1-8E1C-6F345DEC61AD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppSlot.md
ms.openlocfilehash: 3e886803ff608522bd2d563dd9b6cd6effcfe074
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594534"
---
# <span data-ttu-id="63e7b-101">New-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="63e7b-101">New-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="63e7b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63e7b-102">SYNOPSIS</span></span>
<span data-ttu-id="63e7b-103">Azure Web App yuvası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="63e7b-103">Creates an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="63e7b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="63e7b-104">SYNTAX</span></span>

```
New-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [[-AppServicePlan] <String>] [[-SourceWebApp] <Site>] [-IgnoreSourceControl] [-IgnoreCustomHostNames]
 [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>] [[-AseResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="63e7b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="63e7b-105">DESCRIPTION</span></span>
<span data-ttu-id="63e7b-106">**Yeni-AzureRmWebAppSlot** cmdlet 'i, belirtilen App Service planını ve veri merkezini kullanan bir kaynak grubundaki verili bir Azure Web App yuvası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="63e7b-106">The **New-AzureRmWebAppSlot** cmdlet creates an Azure Web App Slot in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="63e7b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="63e7b-107">EXAMPLES</span></span>

### <span data-ttu-id="63e7b-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="63e7b-108">Example 1</span></span>
```
PS C:\> New-AzureRmWebAppSlot -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -Location "West US" -AppServicePlan "ContosoServicePlan" -Slot "Slot001"
```

<span data-ttu-id="63e7b-109">Bu komut, veri merkezi Batı 'da varsayılan-Web-WestUS adlı var olan kaynak grubundaki Contosositesinin mevcut Web App adları altında Slot001 adlı bir yuva oluşturur.</span><span class="sxs-lookup"><span data-stu-id="63e7b-109">This command creates a Slot named Slot001 under an existing Web App names ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="63e7b-110">Bu komut, ContosoServicePlan adında var olan bir App Service planı kullanır.</span><span class="sxs-lookup"><span data-stu-id="63e7b-110">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="63e7b-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="63e7b-111">PARAMETERS</span></span>

### <span data-ttu-id="63e7b-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="63e7b-112">-AppServicePlan</span></span>
<span data-ttu-id="63e7b-113">App Service planı adı</span><span class="sxs-lookup"><span data-stu-id="63e7b-113">App Service Plan Name</span></span>

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

### <span data-ttu-id="63e7b-114">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="63e7b-114">-AppSettingsOverrides</span></span>
<span data-ttu-id="63e7b-115">Uygulama ayarları Hashtable 'ı geçersiz kılıyor</span><span class="sxs-lookup"><span data-stu-id="63e7b-115">App Settings Overrides Hashtable</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63e7b-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="63e7b-116">-AseName</span></span>
<span data-ttu-id="63e7b-117">App Service ortamı adı</span><span class="sxs-lookup"><span data-stu-id="63e7b-117">App Service Environment Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63e7b-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63e7b-118">-AseResourceGroupName</span></span>
<span data-ttu-id="63e7b-119">App Service ortamı kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="63e7b-119">App Service Environment Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63e7b-120">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="63e7b-120">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="63e7b-121">Özel konak adlarını yoksay seçeneği</span><span class="sxs-lookup"><span data-stu-id="63e7b-121">Ignore Custom HostNames Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63e7b-122">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="63e7b-122">-IgnoreSourceControl</span></span>
<span data-ttu-id="63e7b-123">Kaynak denetimi seçeneğini yoksayma</span><span class="sxs-lookup"><span data-stu-id="63e7b-123">Ignore Source Control Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63e7b-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="63e7b-124">-Name</span></span>
<span data-ttu-id="63e7b-125">WEBAPP adı</span><span class="sxs-lookup"><span data-stu-id="63e7b-125">Webapp Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63e7b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63e7b-126">-ResourceGroupName</span></span>
<span data-ttu-id="63e7b-127">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="63e7b-127">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63e7b-128">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="63e7b-128">-Slot</span></span>
<span data-ttu-id="63e7b-129">WEBAPP yuva adı</span><span class="sxs-lookup"><span data-stu-id="63e7b-129">Webapp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63e7b-130">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="63e7b-130">-SourceWebApp</span></span>
<span data-ttu-id="63e7b-131">Kaynak WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="63e7b-131">Source WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="63e7b-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63e7b-132">-DefaultProfile</span></span>
<span data-ttu-id="63e7b-133">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="63e7b-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="63e7b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63e7b-134">CommonParameters</span></span>
<span data-ttu-id="63e7b-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="63e7b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63e7b-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63e7b-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63e7b-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="63e7b-137">INPUTS</span></span>

### <span data-ttu-id="63e7b-138">Bölge</span><span class="sxs-lookup"><span data-stu-id="63e7b-138">Site</span></span>
<span data-ttu-id="63e7b-139">' SourceWebApp ' parametresi ardışık düzenin ' site ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="63e7b-139">Parameter 'SourceWebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="63e7b-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="63e7b-140">OUTPUTS</span></span>

## <span data-ttu-id="63e7b-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="63e7b-141">NOTES</span></span>

## <span data-ttu-id="63e7b-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="63e7b-142">RELATED LINKS</span></span>

[<span data-ttu-id="63e7b-143">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="63e7b-143">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="63e7b-144">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="63e7b-144">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="63e7b-145">Restart-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="63e7b-145">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="63e7b-146">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="63e7b-146">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="63e7b-147">Başlangıç-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="63e7b-147">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="63e7b-148">Dur-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="63e7b-148">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="63e7b-149">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="63e7b-149">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="63e7b-150">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="63e7b-150">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)