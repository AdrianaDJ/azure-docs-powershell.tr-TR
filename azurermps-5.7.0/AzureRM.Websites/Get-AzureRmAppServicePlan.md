---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 89ED4231-7616-47D0-BDAA-D849C245DC79
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmAppServicePlan.md
ms.openlocfilehash: a46d104a6cd5917d6550d6b78d62a6d50581039e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763530"
---
# <span data-ttu-id="0a93b-101">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="0a93b-101">Get-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="0a93b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a93b-102">SYNOPSIS</span></span>
<span data-ttu-id="0a93b-103">Belirtilen kaynak grubunda bir Azure App Service planı alır.</span><span class="sxs-lookup"><span data-stu-id="0a93b-103">Gets an Azure App Service plan in the specified resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0a93b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0a93b-104">SYNTAX</span></span>

### <span data-ttu-id="0a93b-105">S1</span><span class="sxs-lookup"><span data-stu-id="0a93b-105">S1</span></span>
```
Get-AzureRmAppServicePlan [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0a93b-106">S2</span><span class="sxs-lookup"><span data-stu-id="0a93b-106">S2</span></span>
```
Get-AzureRmAppServicePlan [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a93b-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="0a93b-107">DESCRIPTION</span></span>
<span data-ttu-id="0a93b-108">**Get-AzureRmAppServicePlan** cmdlet 'i, belirtilen kaynak grubunda bir Azure App Service planı alır.</span><span class="sxs-lookup"><span data-stu-id="0a93b-108">The **Get-AzureRmAppServicePlan** cmdlet gets an Azure App Service plan in the specified resource group.</span></span>

## <span data-ttu-id="0a93b-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0a93b-109">EXAMPLES</span></span>

### <span data-ttu-id="0a93b-110">Örnek 1: kaynak grubundan bir App Service planı alma</span><span class="sxs-lookup"><span data-stu-id="0a93b-110">Example 1: Get an App Service plan from a resource group</span></span>
```
PS C:\>Get-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="0a93b-111">Bu komut, varsayılan-Web-WestUS adlı kaynak grubuna ait olan ContosoASP adındaki App Service planını alır.</span><span class="sxs-lookup"><span data-stu-id="0a93b-111">This command gets the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

### <span data-ttu-id="0a93b-112">Örnek 2: bir konumdaki tüm App Service planlarını alma</span><span class="sxs-lookup"><span data-stu-id="0a93b-112">Example 2: Get all App Service plans in a location</span></span>
```
PS C:\>Get-AzureRmAppServicePlan -Location "West US"
```

<span data-ttu-id="0a93b-113">Bu komut, "Batı ABD" bölgesinde bulunan tüm App Service planlarını alır.</span><span class="sxs-lookup"><span data-stu-id="0a93b-113">This command gets all App Service plans located in the "West US" region.</span></span>

## <span data-ttu-id="0a93b-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0a93b-114">PARAMETERS</span></span>

### <span data-ttu-id="0a93b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a93b-115">-DefaultProfile</span></span>
<span data-ttu-id="0a93b-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0a93b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0a93b-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="0a93b-117">-Location</span></span>
<span data-ttu-id="0a93b-118">Konumuyla</span><span class="sxs-lookup"><span data-stu-id="0a93b-118">Location</span></span> 

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

### <span data-ttu-id="0a93b-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="0a93b-119">-Name</span></span>
<span data-ttu-id="0a93b-120">App Service planı adı</span><span class="sxs-lookup"><span data-stu-id="0a93b-120">App Service Plan Name</span></span>

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

### <span data-ttu-id="0a93b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a93b-121">-ResourceGroupName</span></span>
<span data-ttu-id="0a93b-122">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="0a93b-122">Resource Group Name</span></span>

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

### <span data-ttu-id="0a93b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a93b-123">CommonParameters</span></span>
<span data-ttu-id="0a93b-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0a93b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a93b-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a93b-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a93b-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0a93b-126">INPUTS</span></span>

### <span data-ttu-id="0a93b-127">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="0a93b-127">None</span></span>
<span data-ttu-id="0a93b-128">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="0a93b-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0a93b-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0a93b-129">OUTPUTS</span></span>

### <span data-ttu-id="0a93b-130">Microsoft. Azure. Management. Websiteleri. modeller. ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="0a93b-130">Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku</span></span>

### <span data-ttu-id="0a93b-131">Microsoft. Azure. Management. Web sitesi. modeller. ServerFarmCollection</span><span class="sxs-lookup"><span data-stu-id="0a93b-131">Microsoft.Azure.Management.WebSites.Models.ServerFarmCollection</span></span>

## <span data-ttu-id="0a93b-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0a93b-132">NOTES</span></span>

## <span data-ttu-id="0a93b-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0a93b-133">RELATED LINKS</span></span>

[<span data-ttu-id="0a93b-134">Yeni-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="0a93b-134">New-AzureRmAppServicePlan</span></span>](./New-AzureRmAppServicePlan.md)

[<span data-ttu-id="0a93b-135">Remove-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="0a93b-135">Remove-AzureRmAppServicePlan</span></span>](./Remove-AzureRmAppServicePlan.md)

[<span data-ttu-id="0a93b-136">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="0a93b-136">Set-AzureRmAppServicePlan</span></span>](./Set-AzureRmAppServicePlan.md)


