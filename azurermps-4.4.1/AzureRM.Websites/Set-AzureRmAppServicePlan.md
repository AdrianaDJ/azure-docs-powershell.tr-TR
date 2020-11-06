---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 32D45795-FBCD-4157-BF45-41BD1F61782E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmAppServicePlan.md
ms.openlocfilehash: 4b6270a6d56b8f210b2f03311bf19bb09950f361
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588227"
---
# <span data-ttu-id="1dff5-101">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="1dff5-101">Set-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="1dff5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1dff5-102">SYNOPSIS</span></span>
<span data-ttu-id="1dff5-103">Bir Azure App Service planı ayarlar.</span><span class="sxs-lookup"><span data-stu-id="1dff5-103">Sets an Azure App Service plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1dff5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1dff5-104">SYNTAX</span></span>

### <span data-ttu-id="1dff5-105">S1</span><span class="sxs-lookup"><span data-stu-id="1dff5-105">S1</span></span>
```
Set-AzureRmAppServicePlan [[-AdminSiteName] <String>] [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [-PerSiteScaling <Boolean>] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1dff5-106">S2</span><span class="sxs-lookup"><span data-stu-id="1dff5-106">S2</span></span>
```
Set-AzureRmAppServicePlan [-AppServicePlan] <ServerFarmWithRichSku> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1dff5-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="1dff5-107">DESCRIPTION</span></span>
<span data-ttu-id="1dff5-108">**Set-AzureRmAppServicePlan** cmdlet 'ı bir Azure App hizmet planı ayarlar.</span><span class="sxs-lookup"><span data-stu-id="1dff5-108">The **Set-AzureRmAppServicePlan** cmdlet sets an Azure App Service plan.</span></span>

## <span data-ttu-id="1dff5-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1dff5-109">EXAMPLES</span></span>

### <span data-ttu-id="1dff5-110">1: App Service planını değiştirme</span><span class="sxs-lookup"><span data-stu-id="1dff5-110">1: Modify an App Service plan</span></span>
```
PS C:\>Set-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -PerSiteScaling $true
```

<span data-ttu-id="1dff5-111">Bu komut, Default-Web-WestUS adlı kaynak grubuna ait olan ContosoASP adlı App Service planındaki Persiteölçeklendirme seçeneğini true olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="1dff5-111">This command sets the PerSiteScaling option to true on the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="1dff5-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1dff5-112">PARAMETERS</span></span>

### <span data-ttu-id="1dff5-113">-Adminsiteadı</span><span class="sxs-lookup"><span data-stu-id="1dff5-113">-AdminSiteName</span></span>
<span data-ttu-id="1dff5-114">Yönetici sitesi adı</span><span class="sxs-lookup"><span data-stu-id="1dff5-114">Admin Site Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dff5-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="1dff5-115">-AppServicePlan</span></span>
<span data-ttu-id="1dff5-116">App Service planı nesnesi</span><span class="sxs-lookup"><span data-stu-id="1dff5-116">App Service Plan Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1dff5-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="1dff5-117">-Name</span></span>
<span data-ttu-id="1dff5-118">App Service planı adı</span><span class="sxs-lookup"><span data-stu-id="1dff5-118">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dff5-119">-Işçilere</span><span class="sxs-lookup"><span data-stu-id="1dff5-119">-NumberofWorkers</span></span>
<span data-ttu-id="1dff5-120">Çalışan sayısı</span><span class="sxs-lookup"><span data-stu-id="1dff5-120">Number Of Workers</span></span>

```yaml
Type: System.Int32
Parameter Sets: S1
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dff5-121">-Persiteölçeklendirme</span><span class="sxs-lookup"><span data-stu-id="1dff5-121">-PerSiteScaling</span></span>
<span data-ttu-id="1dff5-122">Site başına ölçeklendirme Boole değeri</span><span class="sxs-lookup"><span data-stu-id="1dff5-122">Per Site Scaling Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dff5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1dff5-123">-ResourceGroupName</span></span>
<span data-ttu-id="1dff5-124">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="1dff5-124">Resource Group Name</span></span>

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

### <span data-ttu-id="1dff5-125">Katmanlı</span><span class="sxs-lookup"><span data-stu-id="1dff5-125">-Tier</span></span>
<span data-ttu-id="1dff5-126">Katman</span><span class="sxs-lookup"><span data-stu-id="1dff5-126">Tier</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 
Accepted values: Free, Shared, Basic, Standard, Premium

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dff5-127">-WorkerSize</span><span class="sxs-lookup"><span data-stu-id="1dff5-127">-WorkerSize</span></span>
<span data-ttu-id="1dff5-128">Çalışan boyutu</span><span class="sxs-lookup"><span data-stu-id="1dff5-128">Worker Size</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 
Accepted values: Small, Medium, Large, ExtraLarge

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dff5-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dff5-129">-DefaultProfile</span></span>
<span data-ttu-id="1dff5-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1dff5-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1dff5-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dff5-131">CommonParameters</span></span>
<span data-ttu-id="1dff5-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1dff5-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dff5-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1dff5-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dff5-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1dff5-134">INPUTS</span></span>

### <span data-ttu-id="1dff5-135">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="1dff5-135">ServerFarmWithRichSku</span></span>
<span data-ttu-id="1dff5-136">' AppServicePlan ' parametresi ardışık düzenin ' ServerFarmWithRichSku ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="1dff5-136">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="1dff5-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1dff5-137">OUTPUTS</span></span>

### <span data-ttu-id="1dff5-138">Microsoft. Azure. Management. Websiteleri. modeller. ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="1dff5-138">Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku</span></span>

## <span data-ttu-id="1dff5-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1dff5-139">NOTES</span></span>

## <span data-ttu-id="1dff5-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1dff5-140">RELATED LINKS</span></span>

[<span data-ttu-id="1dff5-141">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="1dff5-141">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="1dff5-142">Yeni-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="1dff5-142">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="1dff5-143">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="1dff5-143">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="1dff5-144">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="1dff5-144">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="1dff5-145">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="1dff5-145">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="1dff5-146">Stop-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="1dff5-146">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


