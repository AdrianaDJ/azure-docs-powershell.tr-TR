---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 89ED4231-7616-47D0-BDAA-D849C245DC79
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmAppServicePlan.md
ms.openlocfilehash: 9fe7d3d9580411c31fdf5ca7e21ba1c4379217a4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590796"
---
# <span data-ttu-id="ffb6c-101">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ffb6c-101">Get-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="ffb6c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ffb6c-102">SYNOPSIS</span></span>
<span data-ttu-id="ffb6c-103">Belirtilen kaynak grubunda bir Azure App Service planı alır.</span><span class="sxs-lookup"><span data-stu-id="ffb6c-103">Gets an Azure App Service plan in the specified resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ffb6c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ffb6c-104">SYNTAX</span></span>

### <span data-ttu-id="ffb6c-105">S1</span><span class="sxs-lookup"><span data-stu-id="ffb6c-105">S1</span></span>
```
Get-AzureRmAppServicePlan [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ffb6c-106">S2</span><span class="sxs-lookup"><span data-stu-id="ffb6c-106">S2</span></span>
```
Get-AzureRmAppServicePlan [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ffb6c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="ffb6c-107">DESCRIPTION</span></span>
<span data-ttu-id="ffb6c-108">**Get-AzureRmAppServicePlan** cmdlet 'i, belirtilen kaynak grubunda bir Azure App Service planı alır.</span><span class="sxs-lookup"><span data-stu-id="ffb6c-108">The **Get-AzureRmAppServicePlan** cmdlet gets an Azure App Service plan in the specified resource group.</span></span>

## <span data-ttu-id="ffb6c-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ffb6c-109">EXAMPLES</span></span>

### <span data-ttu-id="ffb6c-110">Örnek 1: kaynak grubundan bir App Service planı alma</span><span class="sxs-lookup"><span data-stu-id="ffb6c-110">Example 1: Get an App Service plan from a resource group</span></span>
```
PS C:\>Get-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="ffb6c-111">Bu komut, varsayılan-Web-WestUS adlı kaynak grubuna ait olan ContosoASP adındaki App Service planını alır.</span><span class="sxs-lookup"><span data-stu-id="ffb6c-111">This command gets the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

### <span data-ttu-id="ffb6c-112">Örnek 2: bir konumdaki tüm App Service planlarını alma</span><span class="sxs-lookup"><span data-stu-id="ffb6c-112">Example 2: Get all App Service plans in a location</span></span>
```
PS C:\>Get-AzureRmAppServicePlan -Location "West US"
```

<span data-ttu-id="ffb6c-113">Bu komut, "Batı ABD" bölgesinde bulunan tüm App Service planlarını alır.</span><span class="sxs-lookup"><span data-stu-id="ffb6c-113">This command gets all App Service plans located in the "West US" region.</span></span>

## <span data-ttu-id="ffb6c-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ffb6c-114">PARAMETERS</span></span>

### <span data-ttu-id="ffb6c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffb6c-115">-DefaultProfile</span></span>
<span data-ttu-id="ffb6c-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ffb6c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ffb6c-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="ffb6c-117">-Location</span></span>
<span data-ttu-id="ffb6c-118">Konumuyla</span><span class="sxs-lookup"><span data-stu-id="ffb6c-118">Location</span></span> 

```yaml
Type: System.String
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffb6c-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="ffb6c-119">-Name</span></span>
<span data-ttu-id="ffb6c-120">App Service planı adı</span><span class="sxs-lookup"><span data-stu-id="ffb6c-120">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffb6c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ffb6c-121">-ResourceGroupName</span></span>
<span data-ttu-id="ffb6c-122">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="ffb6c-122">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffb6c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffb6c-123">CommonParameters</span></span>
<span data-ttu-id="ffb6c-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ffb6c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffb6c-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ffb6c-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffb6c-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ffb6c-126">INPUTS</span></span>

### <span data-ttu-id="ffb6c-127">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="ffb6c-127">None</span></span>

## <span data-ttu-id="ffb6c-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ffb6c-128">OUTPUTS</span></span>

### <span data-ttu-id="ffb6c-129">Microsoft. Azure. Management. Web sitesi. modeller. AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ffb6c-129">Microsoft.Azure.Management.WebSites.Models.AppServicePlan</span></span>

## <span data-ttu-id="ffb6c-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ffb6c-130">NOTES</span></span>

## <span data-ttu-id="ffb6c-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ffb6c-131">RELATED LINKS</span></span>

[<span data-ttu-id="ffb6c-132">Yeni-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ffb6c-132">New-AzureRmAppServicePlan</span></span>](./New-AzureRmAppServicePlan.md)

[<span data-ttu-id="ffb6c-133">Remove-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ffb6c-133">Remove-AzureRmAppServicePlan</span></span>](./Remove-AzureRmAppServicePlan.md)

[<span data-ttu-id="ffb6c-134">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ffb6c-134">Set-AzureRmAppServicePlan</span></span>](./Set-AzureRmAppServicePlan.md)


