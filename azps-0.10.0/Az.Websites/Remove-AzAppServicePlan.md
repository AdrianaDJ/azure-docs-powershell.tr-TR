---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 78AAF476-2E9E-4E60-9940-9A9AC6F9506A
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/remove-Azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Remove-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Remove-AzAppServicePlan.md
ms.openlocfilehash: 3d0e3ad30df71700eb83938181ed86a97a77528a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936084"
---
# <span data-ttu-id="7440d-101">Remove-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="7440d-101">Remove-AzAppServicePlan</span></span>

## <span data-ttu-id="7440d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7440d-102">SYNOPSIS</span></span>
<span data-ttu-id="7440d-103">Azure App hizmet planını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7440d-103">Removes an Azure App Service plan.</span></span>

## <span data-ttu-id="7440d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7440d-104">SYNTAX</span></span>

### <span data-ttu-id="7440d-105">S1</span><span class="sxs-lookup"><span data-stu-id="7440d-105">S1</span></span>
```
Remove-AzAppServicePlan [-Force] [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7440d-106">S2</span><span class="sxs-lookup"><span data-stu-id="7440d-106">S2</span></span>
```
Remove-AzAppServicePlan [-Force] [-AppServicePlan] <AppServicePlan> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7440d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="7440d-107">DESCRIPTION</span></span>
<span data-ttu-id="7440d-108">**Remove-AzAppServicePlan** cmdlet 'ı bir Azure App hizmet planını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7440d-108">The **Remove-AzAppServicePlan** cmdlet removes an Azure App Service plan.</span></span>

## <span data-ttu-id="7440d-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7440d-109">EXAMPLES</span></span>

### <span data-ttu-id="7440d-110">Örnek 1: App Service planını kaldırma</span><span class="sxs-lookup"><span data-stu-id="7440d-110">Example 1: Remove an App Service plan</span></span>
```
PS C:\>Remove-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="7440d-111">Bu komut, varsayılan-Web-WestUS adlı kaynak grubuna ait olan ContosoASP adlı Azure App Service planını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7440d-111">This command removes the Azure App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="7440d-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7440d-112">PARAMETERS</span></span>

### <span data-ttu-id="7440d-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="7440d-113">-AppServicePlan</span></span>
<span data-ttu-id="7440d-114">App Service planı nesnesi</span><span class="sxs-lookup"><span data-stu-id="7440d-114">App Service Plan Object</span></span>

```yaml
Type: AppServicePlan
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7440d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7440d-115">-DefaultProfile</span></span>
<span data-ttu-id="7440d-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7440d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7440d-117">-Force</span><span class="sxs-lookup"><span data-stu-id="7440d-117">-Force</span></span>
<span data-ttu-id="7440d-118">Zorla Kaldır seçeneği</span><span class="sxs-lookup"><span data-stu-id="7440d-118">Forcefully Remove Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7440d-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="7440d-119">-Name</span></span>
<span data-ttu-id="7440d-120">App Service planı adı</span><span class="sxs-lookup"><span data-stu-id="7440d-120">App Service Plan Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7440d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7440d-121">-ResourceGroupName</span></span>
<span data-ttu-id="7440d-122">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="7440d-122">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7440d-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="7440d-123">-Confirm</span></span>
<span data-ttu-id="7440d-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7440d-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7440d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7440d-125">-WhatIf</span></span>
<span data-ttu-id="7440d-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7440d-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7440d-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7440d-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7440d-128">-Iş</span><span class="sxs-lookup"><span data-stu-id="7440d-128">-AsJob</span></span>
<span data-ttu-id="7440d-129">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="7440d-129">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7440d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7440d-130">CommonParameters</span></span>
<span data-ttu-id="7440d-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7440d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7440d-132">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7440d-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7440d-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7440d-133">INPUTS</span></span>

### <span data-ttu-id="7440d-134">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="7440d-134">ServerFarmWithRichSku</span></span>
<span data-ttu-id="7440d-135">' AppServicePlan ' parametresi ardışık düzenin ' ServerFarmWithRichSku ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="7440d-135">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="7440d-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7440d-136">OUTPUTS</span></span>

### <span data-ttu-id="7440d-137">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="7440d-137">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="7440d-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7440d-138">NOTES</span></span>

## <span data-ttu-id="7440d-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7440d-139">RELATED LINKS</span></span>

[<span data-ttu-id="7440d-140">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="7440d-140">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="7440d-141">New-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="7440d-141">New-AzAppServicePlan</span></span>](./New-AzAppServicePlan.md)

[<span data-ttu-id="7440d-142">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="7440d-142">Set-AzAppServicePlan</span></span>](./Set-AzAppServicePlan.md)


