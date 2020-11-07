---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 89ED4231-7616-47D0-BDAA-D849C245DC79
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermappserviceplan
schema: 2.0.0
ms.openlocfilehash: b85d22d1030eaa12e58cded1c7225231c7e8b964
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939033"
---
# <span data-ttu-id="b1fc8-101">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="b1fc8-101">Get-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="b1fc8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1fc8-102">SYNOPSIS</span></span>
<span data-ttu-id="b1fc8-103">Belirtilen kaynak grubunda bir Azure App Service planı alır.</span><span class="sxs-lookup"><span data-stu-id="b1fc8-103">Gets an Azure App Service plan in the specified resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1fc8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b1fc8-104">SYNTAX</span></span>

### <span data-ttu-id="b1fc8-105">S1</span><span class="sxs-lookup"><span data-stu-id="b1fc8-105">S1</span></span>
```
Get-AzureRmAppServicePlan [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1fc8-106">S2</span><span class="sxs-lookup"><span data-stu-id="b1fc8-106">S2</span></span>
```
Get-AzureRmAppServicePlan [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1fc8-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b1fc8-107">DESCRIPTION</span></span>
<span data-ttu-id="b1fc8-108">**Get-AzureRmAppServicePlan** cmdlet 'i, belirtilen kaynak grubunda bir Azure App Service planı alır.</span><span class="sxs-lookup"><span data-stu-id="b1fc8-108">The **Get-AzureRmAppServicePlan** cmdlet gets an Azure App Service plan in the specified resource group.</span></span>

## <span data-ttu-id="b1fc8-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b1fc8-109">EXAMPLES</span></span>

### <span data-ttu-id="b1fc8-110">Örnek 1: kaynak grubundan bir App Service planı alma</span><span class="sxs-lookup"><span data-stu-id="b1fc8-110">Example 1: Get an App Service plan from a resource group</span></span>
```
PS C:\>Get-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="b1fc8-111">Bu komut, varsayılan-Web-WestUS adlı kaynak grubuna ait olan ContosoASP adındaki App Service planını alır.</span><span class="sxs-lookup"><span data-stu-id="b1fc8-111">This command gets the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

### <span data-ttu-id="b1fc8-112">Örnek 2: bir konumdaki tüm App Service planlarını alma</span><span class="sxs-lookup"><span data-stu-id="b1fc8-112">Example 2: Get all App Service plans in a location</span></span>
```
PS C:\>Get-AzureRmAppServicePlan -Location "West US"
```

<span data-ttu-id="b1fc8-113">Bu komut, "Batı ABD" bölgesinde bulunan tüm App Service planlarını alır.</span><span class="sxs-lookup"><span data-stu-id="b1fc8-113">This command gets all App Service plans located in the "West US" region.</span></span>

## <span data-ttu-id="b1fc8-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b1fc8-114">PARAMETERS</span></span>

### <span data-ttu-id="b1fc8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1fc8-115">-DefaultProfile</span></span>
<span data-ttu-id="b1fc8-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b1fc8-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1fc8-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="b1fc8-117">-Location</span></span>
<span data-ttu-id="b1fc8-118">Konumuyla</span><span class="sxs-lookup"><span data-stu-id="b1fc8-118">Location</span></span> 

```yaml
Type: String
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1fc8-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="b1fc8-119">-Name</span></span>
<span data-ttu-id="b1fc8-120">App Service planı adı</span><span class="sxs-lookup"><span data-stu-id="b1fc8-120">App Service Plan Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1fc8-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1fc8-121">-ResourceGroupName</span></span>
<span data-ttu-id="b1fc8-122">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="b1fc8-122">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1fc8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1fc8-123">CommonParameters</span></span>
<span data-ttu-id="b1fc8-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b1fc8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1fc8-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1fc8-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1fc8-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b1fc8-126">INPUTS</span></span>

### <span data-ttu-id="b1fc8-127">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="b1fc8-127">None</span></span>
<span data-ttu-id="b1fc8-128">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="b1fc8-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b1fc8-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b1fc8-129">OUTPUTS</span></span>

### <span data-ttu-id="b1fc8-130">Microsoft. Azure. Management. Websiteleri. modeller. ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="b1fc8-130">Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku</span></span>

### <span data-ttu-id="b1fc8-131">Microsoft. Azure. Management. Web sitesi. modeller. ServerFarmCollection</span><span class="sxs-lookup"><span data-stu-id="b1fc8-131">Microsoft.Azure.Management.WebSites.Models.ServerFarmCollection</span></span>

## <span data-ttu-id="b1fc8-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b1fc8-132">NOTES</span></span>

## <span data-ttu-id="b1fc8-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b1fc8-133">RELATED LINKS</span></span>

[<span data-ttu-id="b1fc8-134">Yeni-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="b1fc8-134">New-AzureRmAppServicePlan</span></span>](./New-AzureRmAppServicePlan.md)

[<span data-ttu-id="b1fc8-135">Remove-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="b1fc8-135">Remove-AzureRmAppServicePlan</span></span>](./Remove-AzureRmAppServicePlan.md)

[<span data-ttu-id="b1fc8-136">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="b1fc8-136">Set-AzureRmAppServicePlan</span></span>](./Set-AzureRmAppServicePlan.md)


