---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 32D45795-FBCD-4157-BF45-41BD1F61782E
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/set-Azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Set-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Set-AzAppServicePlan.md
ms.openlocfilehash: b679b98e84f389e35e7dc291822049e554d40a9a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936063"
---
# <span data-ttu-id="eff69-101">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="eff69-101">Set-AzAppServicePlan</span></span>

## <span data-ttu-id="eff69-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eff69-102">SYNOPSIS</span></span>
<span data-ttu-id="eff69-103">Bir Azure App Service planı ayarlar.</span><span class="sxs-lookup"><span data-stu-id="eff69-103">Sets an Azure App Service plan.</span></span>

## <span data-ttu-id="eff69-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="eff69-104">SYNTAX</span></span>

### <span data-ttu-id="eff69-105">S1</span><span class="sxs-lookup"><span data-stu-id="eff69-105">S1</span></span>
```
Set-AzAppServicePlan [[-AdminSiteName] <String>] [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [-PerSiteScaling <Boolean>] [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eff69-106">S2</span><span class="sxs-lookup"><span data-stu-id="eff69-106">S2</span></span>
```
Set-AzAppServicePlan [-AppServicePlan] <AppServicePlan> [-AsJob]
[-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="eff69-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="eff69-107">DESCRIPTION</span></span>
<span data-ttu-id="eff69-108">**Set-AzAppServicePlan** cmdlet 'ı bir Azure App hizmet planı ayarlar.</span><span class="sxs-lookup"><span data-stu-id="eff69-108">The **Set-AzAppServicePlan** cmdlet sets an Azure App Service plan.</span></span>

## <span data-ttu-id="eff69-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="eff69-109">EXAMPLES</span></span>

### <span data-ttu-id="eff69-110">1: App Service planını değiştirme</span><span class="sxs-lookup"><span data-stu-id="eff69-110">1: Modify an App Service plan</span></span>
```
PS C:\>Set-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -PerSiteScaling $true
```

<span data-ttu-id="eff69-111">Bu komut, Default-Web-WestUS adlı kaynak grubuna ait olan ContosoASP adlı App Service planındaki Persiteölçeklendirme seçeneğini true olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="eff69-111">This command sets the PerSiteScaling option to true on the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="eff69-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="eff69-112">PARAMETERS</span></span>

### <span data-ttu-id="eff69-113">-Adminsiteadı</span><span class="sxs-lookup"><span data-stu-id="eff69-113">-AdminSiteName</span></span>
<span data-ttu-id="eff69-114">Yönetici sitesi adı</span><span class="sxs-lookup"><span data-stu-id="eff69-114">Admin Site Name</span></span>

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

### <span data-ttu-id="eff69-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="eff69-115">-AppServicePlan</span></span>
<span data-ttu-id="eff69-116">App Service planı nesnesi</span><span class="sxs-lookup"><span data-stu-id="eff69-116">App Service Plan Object</span></span>

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

### <span data-ttu-id="eff69-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eff69-117">-DefaultProfile</span></span>
<span data-ttu-id="eff69-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="eff69-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eff69-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="eff69-119">-Name</span></span>
<span data-ttu-id="eff69-120">App Service planı adı</span><span class="sxs-lookup"><span data-stu-id="eff69-120">App Service Plan Name</span></span>

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

### <span data-ttu-id="eff69-121">-Işçilere</span><span class="sxs-lookup"><span data-stu-id="eff69-121">-NumberofWorkers</span></span>
<span data-ttu-id="eff69-122">Çalışan sayısı</span><span class="sxs-lookup"><span data-stu-id="eff69-122">Number Of Workers</span></span>

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

### <span data-ttu-id="eff69-123">-Persiteölçeklendirme</span><span class="sxs-lookup"><span data-stu-id="eff69-123">-PerSiteScaling</span></span>
<span data-ttu-id="eff69-124">Site başına ölçeklendirme Boole değeri</span><span class="sxs-lookup"><span data-stu-id="eff69-124">Per Site Scaling Boolean</span></span>

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

### <span data-ttu-id="eff69-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eff69-125">-ResourceGroupName</span></span>
<span data-ttu-id="eff69-126">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="eff69-126">Resource Group Name</span></span>

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

### <span data-ttu-id="eff69-127">Katmanlı</span><span class="sxs-lookup"><span data-stu-id="eff69-127">-Tier</span></span>
<span data-ttu-id="eff69-128">Katman</span><span class="sxs-lookup"><span data-stu-id="eff69-128">Tier</span></span>

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

### <span data-ttu-id="eff69-129">-WorkerSize</span><span class="sxs-lookup"><span data-stu-id="eff69-129">-WorkerSize</span></span>
<span data-ttu-id="eff69-130">Çalışan boyutu</span><span class="sxs-lookup"><span data-stu-id="eff69-130">Worker Size</span></span>

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
### <span data-ttu-id="eff69-131">-Iş</span><span class="sxs-lookup"><span data-stu-id="eff69-131">-AsJob</span></span>
<span data-ttu-id="eff69-132">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="eff69-132">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="eff69-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eff69-133">CommonParameters</span></span>
<span data-ttu-id="eff69-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="eff69-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eff69-135">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eff69-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eff69-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="eff69-136">INPUTS</span></span>

### <span data-ttu-id="eff69-137">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="eff69-137">ServerFarmWithRichSku</span></span>
<span data-ttu-id="eff69-138">' AppServicePlan ' parametresi ardışık düzenin ' ServerFarmWithRichSku ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="eff69-138">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="eff69-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="eff69-139">OUTPUTS</span></span>

### <span data-ttu-id="eff69-140">Microsoft. Azure. Management. Websiteleri. modeller. ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="eff69-140">Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku</span></span>

## <span data-ttu-id="eff69-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="eff69-141">NOTES</span></span>

## <span data-ttu-id="eff69-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="eff69-142">RELATED LINKS</span></span>

[<span data-ttu-id="eff69-143">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="eff69-143">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="eff69-144">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="eff69-144">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="eff69-145">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="eff69-145">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="eff69-146">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="eff69-146">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="eff69-147">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="eff69-147">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="eff69-148">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="eff69-148">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


