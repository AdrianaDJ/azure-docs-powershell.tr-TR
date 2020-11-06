---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 78AAF476-2E9E-4E60-9940-9A9AC6F9506A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/remove-azurermappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmAppServicePlan.md
ms.openlocfilehash: b97506b8f104859c54c55ee1a937916623f4201d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587084"
---
# <span data-ttu-id="68e97-101">Remove-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="68e97-101">Remove-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="68e97-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68e97-102">SYNOPSIS</span></span>
<span data-ttu-id="68e97-103">Azure App hizmet planını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="68e97-103">Removes an Azure App Service plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="68e97-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="68e97-104">SYNTAX</span></span>

### <span data-ttu-id="68e97-105">S1</span><span class="sxs-lookup"><span data-stu-id="68e97-105">S1</span></span>
```
Remove-AzureRmAppServicePlan [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68e97-106">S2</span><span class="sxs-lookup"><span data-stu-id="68e97-106">S2</span></span>
```
Remove-AzureRmAppServicePlan [-Force] [-AsJob] [-AppServicePlan] <PSAppServicePlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68e97-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="68e97-107">DESCRIPTION</span></span>
<span data-ttu-id="68e97-108">**Remove-AzureRmAppServicePlan** cmdlet 'ı bir Azure App hizmet planını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="68e97-108">The **Remove-AzureRmAppServicePlan** cmdlet removes an Azure App Service plan.</span></span>

## <span data-ttu-id="68e97-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="68e97-109">EXAMPLES</span></span>

### <span data-ttu-id="68e97-110">Örnek 1: App Service planını kaldırma</span><span class="sxs-lookup"><span data-stu-id="68e97-110">Example 1: Remove an App Service plan</span></span>
```
PS C:\>Remove-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="68e97-111">Bu komut, varsayılan-Web-WestUS adlı kaynak grubuna ait olan ContosoASP adlı Azure App Service planını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="68e97-111">This command removes the Azure App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="68e97-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="68e97-112">PARAMETERS</span></span>

### <span data-ttu-id="68e97-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="68e97-113">-AppServicePlan</span></span>
<span data-ttu-id="68e97-114">App Service planı nesnesi</span><span class="sxs-lookup"><span data-stu-id="68e97-114">App Service Plan Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68e97-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="68e97-115">-AsJob</span></span>
<span data-ttu-id="68e97-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="68e97-116">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68e97-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68e97-117">-DefaultProfile</span></span>
<span data-ttu-id="68e97-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="68e97-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="68e97-119">-Force</span><span class="sxs-lookup"><span data-stu-id="68e97-119">-Force</span></span>
<span data-ttu-id="68e97-120">Zorla Kaldır seçeneği</span><span class="sxs-lookup"><span data-stu-id="68e97-120">Forcefully Remove Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68e97-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="68e97-121">-Name</span></span>
<span data-ttu-id="68e97-122">App Service planı adı</span><span class="sxs-lookup"><span data-stu-id="68e97-122">App Service Plan Name</span></span>

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

### <span data-ttu-id="68e97-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68e97-123">-ResourceGroupName</span></span>
<span data-ttu-id="68e97-124">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="68e97-124">Resource Group Name</span></span>

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

### <span data-ttu-id="68e97-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="68e97-125">-Confirm</span></span>
<span data-ttu-id="68e97-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="68e97-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68e97-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68e97-127">-WhatIf</span></span>
<span data-ttu-id="68e97-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="68e97-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68e97-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="68e97-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68e97-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68e97-130">CommonParameters</span></span>
<span data-ttu-id="68e97-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="68e97-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68e97-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68e97-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68e97-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="68e97-133">INPUTS</span></span>

### <span data-ttu-id="68e97-134">Microsoft. Azure. Management. Web sitesi. modeller. AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="68e97-134">Microsoft.Azure.Management.WebSites.Models.AppServicePlan</span></span>
<span data-ttu-id="68e97-135">Parametreler: AppServicePlan (ByValue)</span><span class="sxs-lookup"><span data-stu-id="68e97-135">Parameters: AppServicePlan (ByValue)</span></span>

## <span data-ttu-id="68e97-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="68e97-136">OUTPUTS</span></span>

### <span data-ttu-id="68e97-137">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="68e97-137">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="68e97-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="68e97-138">NOTES</span></span>

## <span data-ttu-id="68e97-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="68e97-139">RELATED LINKS</span></span>

[<span data-ttu-id="68e97-140">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="68e97-140">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="68e97-141">Yeni-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="68e97-141">New-AzureRmAppServicePlan</span></span>](./New-AzureRmAppServicePlan.md)

[<span data-ttu-id="68e97-142">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="68e97-142">Set-AzureRmAppServicePlan</span></span>](./Set-AzureRmAppServicePlan.md)


