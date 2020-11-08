---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 89ED4231-7616-47D0-BDAA-D849C245DC79
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzAppServicePlan.md
ms.openlocfilehash: 064ccbcfa94137f5221a5d08e0a06e09328e0b1f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93934379"
---
# <span data-ttu-id="0ea1d-101">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="0ea1d-101">Get-AzAppServicePlan</span></span>

## <span data-ttu-id="0ea1d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ea1d-102">SYNOPSIS</span></span>
<span data-ttu-id="0ea1d-103">Belirtilen kaynak grubunda bir Azure App Service planı alır.</span><span class="sxs-lookup"><span data-stu-id="0ea1d-103">Gets an Azure App Service plan in the specified resource group.</span></span>

## <span data-ttu-id="0ea1d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0ea1d-104">SYNTAX</span></span>

### <span data-ttu-id="0ea1d-105">S1</span><span class="sxs-lookup"><span data-stu-id="0ea1d-105">S1</span></span>
```
Get-AzAppServicePlan [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0ea1d-106">S2</span><span class="sxs-lookup"><span data-stu-id="0ea1d-106">S2</span></span>
```
Get-AzAppServicePlan [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ea1d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="0ea1d-107">DESCRIPTION</span></span>
<span data-ttu-id="0ea1d-108">**Get-AzAppServicePlan** cmdlet 'i, belirtilen kaynak grubunda bir Azure App Service planı alır.</span><span class="sxs-lookup"><span data-stu-id="0ea1d-108">The **Get-AzAppServicePlan** cmdlet gets an Azure App Service plan in the specified resource group.</span></span>

## <span data-ttu-id="0ea1d-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0ea1d-109">EXAMPLES</span></span>

### <span data-ttu-id="0ea1d-110">Örnek 1: kaynak grubundan bir App Service planı alma</span><span class="sxs-lookup"><span data-stu-id="0ea1d-110">Example 1: Get an App Service plan from a resource group</span></span>
```
PS C:\>Get-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="0ea1d-111">Bu komut, varsayılan-Web-WestUS adlı kaynak grubuna ait olan ContosoASP adındaki App Service planını alır.</span><span class="sxs-lookup"><span data-stu-id="0ea1d-111">This command gets the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

### <span data-ttu-id="0ea1d-112">Örnek 2: bir konumdaki tüm App Service planlarını alma</span><span class="sxs-lookup"><span data-stu-id="0ea1d-112">Example 2: Get all App Service plans in a location</span></span>
```
PS C:\>Get-AzAppServicePlan -Location "West US"
```

<span data-ttu-id="0ea1d-113">Bu komut, "Batı ABD" bölgesinde bulunan tüm App Service planlarını alır.</span><span class="sxs-lookup"><span data-stu-id="0ea1d-113">This command gets all App Service plans located in the "West US" region.</span></span>

## <span data-ttu-id="0ea1d-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0ea1d-114">PARAMETERS</span></span>

### <span data-ttu-id="0ea1d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ea1d-115">-DefaultProfile</span></span>
<span data-ttu-id="0ea1d-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0ea1d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ea1d-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="0ea1d-117">-Location</span></span>
<span data-ttu-id="0ea1d-118">Konumuyla</span><span class="sxs-lookup"><span data-stu-id="0ea1d-118">Location</span></span> 

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

### <span data-ttu-id="0ea1d-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="0ea1d-119">-Name</span></span>
<span data-ttu-id="0ea1d-120">App Service planı adı</span><span class="sxs-lookup"><span data-stu-id="0ea1d-120">App Service Plan Name</span></span>

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

### <span data-ttu-id="0ea1d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ea1d-121">-ResourceGroupName</span></span>
<span data-ttu-id="0ea1d-122">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="0ea1d-122">Resource Group Name</span></span>

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

### <span data-ttu-id="0ea1d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ea1d-123">CommonParameters</span></span>
<span data-ttu-id="0ea1d-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0ea1d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ea1d-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ea1d-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ea1d-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0ea1d-126">INPUTS</span></span>

### <span data-ttu-id="0ea1d-127">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="0ea1d-127">None</span></span>

## <span data-ttu-id="0ea1d-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0ea1d-128">OUTPUTS</span></span>

### <span data-ttu-id="0ea1d-129">Microsoft. Azure. Commands. WebApps. modeller. WebApp. PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="0ea1d-129">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="0ea1d-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0ea1d-130">NOTES</span></span>

## <span data-ttu-id="0ea1d-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0ea1d-131">RELATED LINKS</span></span>

[<span data-ttu-id="0ea1d-132">New-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="0ea1d-132">New-AzAppServicePlan</span></span>](./New-AzAppServicePlan.md)

[<span data-ttu-id="0ea1d-133">Remove-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="0ea1d-133">Remove-AzAppServicePlan</span></span>](./Remove-AzAppServicePlan.md)

[<span data-ttu-id="0ea1d-134">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="0ea1d-134">Set-AzAppServicePlan</span></span>](./Set-AzAppServicePlan.md)

