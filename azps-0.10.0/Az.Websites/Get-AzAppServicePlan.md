---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 89ED4231-7616-47D0-BDAA-D849C245DC79
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzAppServicePlan.md
ms.openlocfilehash: 48d37bf19ec6613ce1f42ee8cf7609bd6383e12f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936128"
---
# <span data-ttu-id="3548e-101">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="3548e-101">Get-AzAppServicePlan</span></span>

## <span data-ttu-id="3548e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3548e-102">SYNOPSIS</span></span>
<span data-ttu-id="3548e-103">Belirtilen kaynak grubunda bir Azure App Service planı alır.</span><span class="sxs-lookup"><span data-stu-id="3548e-103">Gets an Azure App Service plan in the specified resource group.</span></span>

## <span data-ttu-id="3548e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3548e-104">SYNTAX</span></span>

### <span data-ttu-id="3548e-105">S1</span><span class="sxs-lookup"><span data-stu-id="3548e-105">S1</span></span>
```
Get-AzAppServicePlan [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3548e-106">S2</span><span class="sxs-lookup"><span data-stu-id="3548e-106">S2</span></span>
```
Get-AzAppServicePlan [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3548e-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="3548e-107">DESCRIPTION</span></span>
<span data-ttu-id="3548e-108">**Get-AzAppServicePlan** cmdlet 'i, belirtilen kaynak grubunda bir Azure App Service planı alır.</span><span class="sxs-lookup"><span data-stu-id="3548e-108">The **Get-AzAppServicePlan** cmdlet gets an Azure App Service plan in the specified resource group.</span></span>

## <span data-ttu-id="3548e-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3548e-109">EXAMPLES</span></span>

### <span data-ttu-id="3548e-110">Örnek 1: kaynak grubundan bir App Service planı alma</span><span class="sxs-lookup"><span data-stu-id="3548e-110">Example 1: Get an App Service plan from a resource group</span></span>
```
PS C:\>Get-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="3548e-111">Bu komut, varsayılan-Web-WestUS adlı kaynak grubuna ait olan ContosoASP adındaki App Service planını alır.</span><span class="sxs-lookup"><span data-stu-id="3548e-111">This command gets the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

### <span data-ttu-id="3548e-112">Örnek 2: bir konumdaki tüm App Service planlarını alma</span><span class="sxs-lookup"><span data-stu-id="3548e-112">Example 2: Get all App Service plans in a location</span></span>
```
PS C:\>Get-AzAppServicePlan -Location "West US"
```

<span data-ttu-id="3548e-113">Bu komut, "Batı ABD" bölgesinde bulunan tüm App Service planlarını alır.</span><span class="sxs-lookup"><span data-stu-id="3548e-113">This command gets all App Service plans located in the "West US" region.</span></span>

## <span data-ttu-id="3548e-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3548e-114">PARAMETERS</span></span>

### <span data-ttu-id="3548e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3548e-115">-DefaultProfile</span></span>
<span data-ttu-id="3548e-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3548e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3548e-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="3548e-117">-Location</span></span>
<span data-ttu-id="3548e-118">Konumuyla</span><span class="sxs-lookup"><span data-stu-id="3548e-118">Location</span></span> 

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

### <span data-ttu-id="3548e-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="3548e-119">-Name</span></span>
<span data-ttu-id="3548e-120">App Service planı adı</span><span class="sxs-lookup"><span data-stu-id="3548e-120">App Service Plan Name</span></span>

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

### <span data-ttu-id="3548e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3548e-121">-ResourceGroupName</span></span>
<span data-ttu-id="3548e-122">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="3548e-122">Resource Group Name</span></span>

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

### <span data-ttu-id="3548e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3548e-123">CommonParameters</span></span>
<span data-ttu-id="3548e-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3548e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3548e-125">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3548e-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3548e-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3548e-126">INPUTS</span></span>

### <span data-ttu-id="3548e-127">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="3548e-127">None</span></span>
<span data-ttu-id="3548e-128">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="3548e-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3548e-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3548e-129">OUTPUTS</span></span>

### <span data-ttu-id="3548e-130">Microsoft. Azure. Management. Websiteleri. modeller. ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="3548e-130">Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku</span></span>

### <span data-ttu-id="3548e-131">Microsoft. Azure. Management. Web sitesi. modeller. ServerFarmCollection</span><span class="sxs-lookup"><span data-stu-id="3548e-131">Microsoft.Azure.Management.WebSites.Models.ServerFarmCollection</span></span>

## <span data-ttu-id="3548e-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3548e-132">NOTES</span></span>

## <span data-ttu-id="3548e-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3548e-133">RELATED LINKS</span></span>

[<span data-ttu-id="3548e-134">New-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="3548e-134">New-AzAppServicePlan</span></span>](./New-AzAppServicePlan.md)

[<span data-ttu-id="3548e-135">Remove-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="3548e-135">Remove-AzAppServicePlan</span></span>](./Remove-AzAppServicePlan.md)

[<span data-ttu-id="3548e-136">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="3548e-136">Set-AzAppServicePlan</span></span>](./Set-AzAppServicePlan.md)


