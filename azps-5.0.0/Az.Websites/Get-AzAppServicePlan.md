---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 89ED4231-7616-47D0-BDAA-D849C245DC79
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzAppServicePlan.md
ms.openlocfilehash: afbee0d6b13c1ce42931a2379cff6aa7ee0127b9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324142"
---
# <span data-ttu-id="cba79-101">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="cba79-101">Get-AzAppServicePlan</span></span>

## <span data-ttu-id="cba79-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cba79-102">SYNOPSIS</span></span>
<span data-ttu-id="cba79-103">Belirtilen kaynak grubunda bir Azure App Service planı alır.</span><span class="sxs-lookup"><span data-stu-id="cba79-103">Gets an Azure App Service plan in the specified resource group.</span></span>

## <span data-ttu-id="cba79-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cba79-104">SYNTAX</span></span>

### <span data-ttu-id="cba79-105">S1</span><span class="sxs-lookup"><span data-stu-id="cba79-105">S1</span></span>
```
Get-AzAppServicePlan [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cba79-106">S2</span><span class="sxs-lookup"><span data-stu-id="cba79-106">S2</span></span>
```
Get-AzAppServicePlan [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cba79-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="cba79-107">DESCRIPTION</span></span>
<span data-ttu-id="cba79-108">**Get-AzAppServicePlan** cmdlet 'i, belirtilen kaynak grubunda bir Azure App Service planı alır.</span><span class="sxs-lookup"><span data-stu-id="cba79-108">The **Get-AzAppServicePlan** cmdlet gets an Azure App Service plan in the specified resource group.</span></span>

## <span data-ttu-id="cba79-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cba79-109">EXAMPLES</span></span>

### <span data-ttu-id="cba79-110">Örnek 1: kaynak grubundan bir App Service planı alma</span><span class="sxs-lookup"><span data-stu-id="cba79-110">Example 1: Get an App Service plan from a resource group</span></span>
```
PS C:\>Get-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="cba79-111">Bu komut, varsayılan-Web-WestUS adlı kaynak grubuna ait olan ContosoASP adındaki App Service planını alır.</span><span class="sxs-lookup"><span data-stu-id="cba79-111">This command gets the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

### <span data-ttu-id="cba79-112">Örnek 2: bir konumdaki tüm App Service planlarını alma</span><span class="sxs-lookup"><span data-stu-id="cba79-112">Example 2: Get all App Service plans in a location</span></span>
```
PS C:\>Get-AzAppServicePlan -Location "West US"
```

<span data-ttu-id="cba79-113">Bu komut, "Batı ABD" bölgesinde bulunan tüm App Service planlarını alır.</span><span class="sxs-lookup"><span data-stu-id="cba79-113">This command gets all App Service plans located in the "West US" region.</span></span>

## <span data-ttu-id="cba79-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cba79-114">PARAMETERS</span></span>

### <span data-ttu-id="cba79-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cba79-115">-DefaultProfile</span></span>
<span data-ttu-id="cba79-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cba79-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cba79-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="cba79-117">-Location</span></span>
<span data-ttu-id="cba79-118">Konumuyla</span><span class="sxs-lookup"><span data-stu-id="cba79-118">Location</span></span> 

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

### <span data-ttu-id="cba79-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="cba79-119">-Name</span></span>
<span data-ttu-id="cba79-120">App Service planı adı</span><span class="sxs-lookup"><span data-stu-id="cba79-120">App Service Plan Name</span></span>

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

### <span data-ttu-id="cba79-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cba79-121">-ResourceGroupName</span></span>
<span data-ttu-id="cba79-122">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="cba79-122">Resource Group Name</span></span>

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

### <span data-ttu-id="cba79-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cba79-123">CommonParameters</span></span>
<span data-ttu-id="cba79-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cba79-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cba79-125">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cba79-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cba79-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cba79-126">INPUTS</span></span>

### <span data-ttu-id="cba79-127">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="cba79-127">None</span></span>

## <span data-ttu-id="cba79-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cba79-128">OUTPUTS</span></span>

### <span data-ttu-id="cba79-129">Microsoft. Azure. Commands. WebApps. modeller. WebApp. PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="cba79-129">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="cba79-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cba79-130">NOTES</span></span>

## <span data-ttu-id="cba79-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cba79-131">RELATED LINKS</span></span>

[<span data-ttu-id="cba79-132">New-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="cba79-132">New-AzAppServicePlan</span></span>](./New-AzAppServicePlan.md)

[<span data-ttu-id="cba79-133">Remove-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="cba79-133">Remove-AzAppServicePlan</span></span>](./Remove-AzAppServicePlan.md)

[<span data-ttu-id="cba79-134">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="cba79-134">Set-AzAppServicePlan</span></span>](./Set-AzAppServicePlan.md)


