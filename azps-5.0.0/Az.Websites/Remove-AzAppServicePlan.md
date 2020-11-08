---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 78AAF476-2E9E-4E60-9940-9A9AC6F9506A
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzAppServicePlan.md
ms.openlocfilehash: dfd2cfd20ab11e2e70e03dc3e166c83729ef344a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279261"
---
# <span data-ttu-id="1dbc3-101">Remove-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="1dbc3-101">Remove-AzAppServicePlan</span></span>

## <span data-ttu-id="1dbc3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1dbc3-102">SYNOPSIS</span></span>
<span data-ttu-id="1dbc3-103">Azure App hizmet planını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1dbc3-103">Removes an Azure App Service plan.</span></span>

## <span data-ttu-id="1dbc3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1dbc3-104">SYNTAX</span></span>

### <span data-ttu-id="1dbc3-105">S1</span><span class="sxs-lookup"><span data-stu-id="1dbc3-105">S1</span></span>
```
Remove-AzAppServicePlan [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1dbc3-106">S2</span><span class="sxs-lookup"><span data-stu-id="1dbc3-106">S2</span></span>
```
Remove-AzAppServicePlan [-Force] [-AsJob] [-AppServicePlan] <PSAppServicePlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1dbc3-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="1dbc3-107">DESCRIPTION</span></span>
<span data-ttu-id="1dbc3-108">**Remove-AzAppServicePlan** cmdlet 'ı bir Azure App hizmet planını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1dbc3-108">The **Remove-AzAppServicePlan** cmdlet removes an Azure App Service plan.</span></span>

## <span data-ttu-id="1dbc3-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1dbc3-109">EXAMPLES</span></span>

### <span data-ttu-id="1dbc3-110">Örnek 1: App Service planını kaldırma</span><span class="sxs-lookup"><span data-stu-id="1dbc3-110">Example 1: Remove an App Service plan</span></span>
```
PS C:\>Remove-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="1dbc3-111">Bu komut, varsayılan-Web-WestUS adlı kaynak grubuna ait olan ContosoASP adlı Azure App Service planını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1dbc3-111">This command removes the Azure App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="1dbc3-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1dbc3-112">PARAMETERS</span></span>

### <span data-ttu-id="1dbc3-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="1dbc3-113">-AppServicePlan</span></span>
<span data-ttu-id="1dbc3-114">App Service planı nesnesi</span><span class="sxs-lookup"><span data-stu-id="1dbc3-114">App Service Plan Object</span></span>

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

### <span data-ttu-id="1dbc3-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="1dbc3-115">-AsJob</span></span>
<span data-ttu-id="1dbc3-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="1dbc3-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1dbc3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dbc3-117">-DefaultProfile</span></span>
<span data-ttu-id="1dbc3-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1dbc3-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1dbc3-119">-Force</span><span class="sxs-lookup"><span data-stu-id="1dbc3-119">-Force</span></span>
<span data-ttu-id="1dbc3-120">Zorla Kaldır seçeneği</span><span class="sxs-lookup"><span data-stu-id="1dbc3-120">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="1dbc3-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="1dbc3-121">-Name</span></span>
<span data-ttu-id="1dbc3-122">App Service planı adı</span><span class="sxs-lookup"><span data-stu-id="1dbc3-122">App Service Plan Name</span></span>

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

### <span data-ttu-id="1dbc3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1dbc3-123">-ResourceGroupName</span></span>
<span data-ttu-id="1dbc3-124">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="1dbc3-124">Resource Group Name</span></span>

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

### <span data-ttu-id="1dbc3-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="1dbc3-125">-Confirm</span></span>
<span data-ttu-id="1dbc3-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1dbc3-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1dbc3-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1dbc3-127">-WhatIf</span></span>
<span data-ttu-id="1dbc3-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1dbc3-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1dbc3-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1dbc3-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1dbc3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dbc3-130">CommonParameters</span></span>
<span data-ttu-id="1dbc3-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1dbc3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dbc3-132">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1dbc3-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dbc3-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1dbc3-133">INPUTS</span></span>

### <span data-ttu-id="1dbc3-134">Microsoft. Azure. Commands. WebApps. modeller. WebApp. PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="1dbc3-134">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="1dbc3-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1dbc3-135">OUTPUTS</span></span>

### <span data-ttu-id="1dbc3-136">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="1dbc3-136">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="1dbc3-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1dbc3-137">NOTES</span></span>

## <span data-ttu-id="1dbc3-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1dbc3-138">RELATED LINKS</span></span>

[<span data-ttu-id="1dbc3-139">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="1dbc3-139">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="1dbc3-140">New-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="1dbc3-140">New-AzAppServicePlan</span></span>](./New-AzAppServicePlan.md)

[<span data-ttu-id="1dbc3-141">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="1dbc3-141">Set-AzAppServicePlan</span></span>](./Set-AzAppServicePlan.md)


