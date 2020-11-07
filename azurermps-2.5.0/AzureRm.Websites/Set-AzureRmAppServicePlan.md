---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 32D45795-FBCD-4157-BF45-41BD1F61782E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/set-azurermappserviceplan
schema: 2.0.0
ms.openlocfilehash: eac153c22a576686feb15b75f3180ed4fb12ec94
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939816"
---
# <span data-ttu-id="c2deb-101">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="c2deb-101">Set-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="c2deb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2deb-102">SYNOPSIS</span></span>
<span data-ttu-id="c2deb-103">Bir Azure App Service planı ayarlar.</span><span class="sxs-lookup"><span data-stu-id="c2deb-103">Sets an Azure App Service plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c2deb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c2deb-104">SYNTAX</span></span>

### <span data-ttu-id="c2deb-105">S1</span><span class="sxs-lookup"><span data-stu-id="c2deb-105">S1</span></span>
```
Set-AzureRmAppServicePlan [[-AdminSiteName] <String>] [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [-PerSiteScaling <Boolean>] [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2deb-106">S2</span><span class="sxs-lookup"><span data-stu-id="c2deb-106">S2</span></span>
```
Set-AzureRmAppServicePlan [-AppServicePlan] <AppServicePlan> [-AsJob]
[-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c2deb-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="c2deb-107">DESCRIPTION</span></span>
<span data-ttu-id="c2deb-108">**Set-AzureRmAppServicePlan** cmdlet 'ı bir Azure App hizmet planı ayarlar.</span><span class="sxs-lookup"><span data-stu-id="c2deb-108">The **Set-AzureRmAppServicePlan** cmdlet sets an Azure App Service plan.</span></span>

## <span data-ttu-id="c2deb-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c2deb-109">EXAMPLES</span></span>

### <span data-ttu-id="c2deb-110">1: App Service planını değiştirme</span><span class="sxs-lookup"><span data-stu-id="c2deb-110">1: Modify an App Service plan</span></span>
```
PS C:\>Set-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -PerSiteScaling $true
```

<span data-ttu-id="c2deb-111">Bu komut, Default-Web-WestUS adlı kaynak grubuna ait olan ContosoASP adlı App Service planındaki Persiteölçeklendirme seçeneğini true olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="c2deb-111">This command sets the PerSiteScaling option to true on the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="c2deb-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c2deb-112">PARAMETERS</span></span>

### <span data-ttu-id="c2deb-113">-Adminsiteadı</span><span class="sxs-lookup"><span data-stu-id="c2deb-113">-AdminSiteName</span></span>
<span data-ttu-id="c2deb-114">Yönetici sitesi adı</span><span class="sxs-lookup"><span data-stu-id="c2deb-114">Admin Site Name</span></span>

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

### <span data-ttu-id="c2deb-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="c2deb-115">-AppServicePlan</span></span>
<span data-ttu-id="c2deb-116">App Service planı nesnesi</span><span class="sxs-lookup"><span data-stu-id="c2deb-116">App Service Plan Object</span></span>

```yaml
Type: AppServicePlan
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2deb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2deb-117">-DefaultProfile</span></span>
<span data-ttu-id="c2deb-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c2deb-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2deb-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="c2deb-119">-Name</span></span>
<span data-ttu-id="c2deb-120">App Service planı adı</span><span class="sxs-lookup"><span data-stu-id="c2deb-120">App Service Plan Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2deb-121">-Işçilere</span><span class="sxs-lookup"><span data-stu-id="c2deb-121">-NumberofWorkers</span></span>
<span data-ttu-id="c2deb-122">Çalışan sayısı</span><span class="sxs-lookup"><span data-stu-id="c2deb-122">Number Of Workers</span></span>

```yaml
Type: Int32
Parameter Sets: S1
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2deb-123">-Persiteölçeklendirme</span><span class="sxs-lookup"><span data-stu-id="c2deb-123">-PerSiteScaling</span></span>
<span data-ttu-id="c2deb-124">Site başına ölçeklendirme Boole değeri</span><span class="sxs-lookup"><span data-stu-id="c2deb-124">Per Site Scaling Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2deb-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2deb-125">-ResourceGroupName</span></span>
<span data-ttu-id="c2deb-126">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="c2deb-126">Resource Group Name</span></span>

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

### <span data-ttu-id="c2deb-127">Katmanlı</span><span class="sxs-lookup"><span data-stu-id="c2deb-127">-Tier</span></span>
<span data-ttu-id="c2deb-128">Katman</span><span class="sxs-lookup"><span data-stu-id="c2deb-128">Tier</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 
Accepted values: Free, Shared, Basic, Standard, Premium, PremiumV2

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2deb-129">-WorkerSize</span><span class="sxs-lookup"><span data-stu-id="c2deb-129">-WorkerSize</span></span>
<span data-ttu-id="c2deb-130">Çalışan boyutu</span><span class="sxs-lookup"><span data-stu-id="c2deb-130">Worker Size</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 
Accepted values: Small, Medium, Large, ExtraLarge

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="c2deb-131">-Iş</span><span class="sxs-lookup"><span data-stu-id="c2deb-131">-AsJob</span></span>
<span data-ttu-id="c2deb-132">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="c2deb-132">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c2deb-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2deb-133">CommonParameters</span></span>
<span data-ttu-id="c2deb-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c2deb-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2deb-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2deb-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2deb-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c2deb-136">INPUTS</span></span>

### <span data-ttu-id="c2deb-137">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="c2deb-137">ServerFarmWithRichSku</span></span>
<span data-ttu-id="c2deb-138">' AppServicePlan ' parametresi ardışık düzenin ' ServerFarmWithRichSku ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="c2deb-138">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="c2deb-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c2deb-139">OUTPUTS</span></span>

### <span data-ttu-id="c2deb-140">Microsoft. Azure. Management. Websiteleri. modeller. ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="c2deb-140">Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku</span></span>

## <span data-ttu-id="c2deb-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c2deb-141">NOTES</span></span>

## <span data-ttu-id="c2deb-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c2deb-142">RELATED LINKS</span></span>

[<span data-ttu-id="c2deb-143">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="c2deb-143">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="c2deb-144">Yeni-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="c2deb-144">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="c2deb-145">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="c2deb-145">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="c2deb-146">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="c2deb-146">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="c2deb-147">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="c2deb-147">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="c2deb-148">Stop-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="c2deb-148">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


