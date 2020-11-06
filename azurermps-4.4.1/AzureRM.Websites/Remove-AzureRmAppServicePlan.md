---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 78AAF476-2E9E-4E60-9940-9A9AC6F9506A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmAppServicePlan.md
ms.openlocfilehash: d1d07e27a7ad6fb6059cbfc8e4c972b1cedaf7e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594533"
---
# <span data-ttu-id="8b045-101">Remove-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="8b045-101">Remove-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="8b045-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b045-102">SYNOPSIS</span></span>
<span data-ttu-id="8b045-103">Azure App hizmet planını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8b045-103">Removes an Azure App Service plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8b045-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8b045-104">SYNTAX</span></span>

### <span data-ttu-id="8b045-105">S1</span><span class="sxs-lookup"><span data-stu-id="8b045-105">S1</span></span>
```
Remove-AzureRmAppServicePlan [-Force] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b045-106">S2</span><span class="sxs-lookup"><span data-stu-id="8b045-106">S2</span></span>
```
Remove-AzureRmAppServicePlan [-Force] [-AppServicePlan] <ServerFarmWithRichSku>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b045-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="8b045-107">DESCRIPTION</span></span>
<span data-ttu-id="8b045-108">**Remove-AzureRmAppServicePlan** cmdlet 'ı bir Azure App hizmet planını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8b045-108">The **Remove-AzureRmAppServicePlan** cmdlet removes an Azure App Service plan.</span></span>

## <span data-ttu-id="8b045-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8b045-109">EXAMPLES</span></span>

### <span data-ttu-id="8b045-110">Örnek 1: App Service planını kaldırma</span><span class="sxs-lookup"><span data-stu-id="8b045-110">Example 1: Remove an App Service plan</span></span>
```
PS C:\>Remove-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="8b045-111">Bu komut, varsayılan-Web-WestUS adlı kaynak grubuna ait olan ContosoASP adlı Azure App Service planını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8b045-111">This command removes the Azure App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="8b045-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8b045-112">PARAMETERS</span></span>

### <span data-ttu-id="8b045-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="8b045-113">-AppServicePlan</span></span>
<span data-ttu-id="8b045-114">App Service planı nesnesi</span><span class="sxs-lookup"><span data-stu-id="8b045-114">App Service Plan Object</span></span>

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

### <span data-ttu-id="8b045-115">-Force</span><span class="sxs-lookup"><span data-stu-id="8b045-115">-Force</span></span>
<span data-ttu-id="8b045-116">Zorla Kaldır seçeneği</span><span class="sxs-lookup"><span data-stu-id="8b045-116">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="8b045-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="8b045-117">-Name</span></span>
<span data-ttu-id="8b045-118">App Service planı adı</span><span class="sxs-lookup"><span data-stu-id="8b045-118">App Service Plan Name</span></span>

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

### <span data-ttu-id="8b045-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b045-119">-ResourceGroupName</span></span>
<span data-ttu-id="8b045-120">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="8b045-120">Resource Group Name</span></span>

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

### <span data-ttu-id="8b045-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="8b045-121">-Confirm</span></span>
<span data-ttu-id="8b045-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8b045-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b045-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b045-123">-WhatIf</span></span>
<span data-ttu-id="8b045-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8b045-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b045-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8b045-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b045-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b045-126">-DefaultProfile</span></span>
<span data-ttu-id="8b045-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8b045-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8b045-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b045-128">CommonParameters</span></span>
<span data-ttu-id="8b045-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8b045-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b045-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b045-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b045-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8b045-131">INPUTS</span></span>

### <span data-ttu-id="8b045-132">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="8b045-132">ServerFarmWithRichSku</span></span>
<span data-ttu-id="8b045-133">' AppServicePlan ' parametresi ardışık düzenin ' ServerFarmWithRichSku ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="8b045-133">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="8b045-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8b045-134">OUTPUTS</span></span>

### <span data-ttu-id="8b045-135">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="8b045-135">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="8b045-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8b045-136">NOTES</span></span>

## <span data-ttu-id="8b045-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8b045-137">RELATED LINKS</span></span>

[<span data-ttu-id="8b045-138">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="8b045-138">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="8b045-139">Yeni-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="8b045-139">New-AzureRmAppServicePlan</span></span>](./New-AzureRmAppServicePlan.md)

[<span data-ttu-id="8b045-140">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="8b045-140">Set-AzureRmAppServicePlan</span></span>](./Set-AzureRmAppServicePlan.md)


