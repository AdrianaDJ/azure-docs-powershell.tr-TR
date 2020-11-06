---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 78AAF476-2E9E-4E60-9940-9A9AC6F9506A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/remove-azurermappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmAppServicePlan.md
ms.openlocfilehash: d5164e47dd759538fea6f0ab143ef9640055f1c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588676"
---
# <span data-ttu-id="3cedd-101">Remove-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="3cedd-101">Remove-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="3cedd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3cedd-102">SYNOPSIS</span></span>
<span data-ttu-id="3cedd-103">Azure App hizmet planını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3cedd-103">Removes an Azure App Service plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3cedd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3cedd-104">SYNTAX</span></span>

### <span data-ttu-id="3cedd-105">S1</span><span class="sxs-lookup"><span data-stu-id="3cedd-105">S1</span></span>
```
Remove-AzureRmAppServicePlan [-Force] [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cedd-106">S2</span><span class="sxs-lookup"><span data-stu-id="3cedd-106">S2</span></span>
```
Remove-AzureRmAppServicePlan [-Force] [-AppServicePlan] <ServerFarmWithRichSku> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3cedd-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="3cedd-107">DESCRIPTION</span></span>
<span data-ttu-id="3cedd-108">**Remove-AzureRmAppServicePlan** cmdlet 'ı bir Azure App hizmet planını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3cedd-108">The **Remove-AzureRmAppServicePlan** cmdlet removes an Azure App Service plan.</span></span>

## <span data-ttu-id="3cedd-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3cedd-109">EXAMPLES</span></span>

### <span data-ttu-id="3cedd-110">Örnek 1: App Service planını kaldırma</span><span class="sxs-lookup"><span data-stu-id="3cedd-110">Example 1: Remove an App Service plan</span></span>
```
PS C:\>Remove-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="3cedd-111">Bu komut, varsayılan-Web-WestUS adlı kaynak grubuna ait olan ContosoASP adlı Azure App Service planını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3cedd-111">This command removes the Azure App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="3cedd-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3cedd-112">PARAMETERS</span></span>

### <span data-ttu-id="3cedd-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="3cedd-113">-AppServicePlan</span></span>
<span data-ttu-id="3cedd-114">App Service planı nesnesi</span><span class="sxs-lookup"><span data-stu-id="3cedd-114">App Service Plan Object</span></span>

```yaml
Type: ServerFarmWithRichSku
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3cedd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cedd-115">-DefaultProfile</span></span>
<span data-ttu-id="3cedd-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3cedd-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3cedd-117">-Force</span><span class="sxs-lookup"><span data-stu-id="3cedd-117">-Force</span></span>
<span data-ttu-id="3cedd-118">Zorla Kaldır seçeneği</span><span class="sxs-lookup"><span data-stu-id="3cedd-118">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="3cedd-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="3cedd-119">-Name</span></span>
<span data-ttu-id="3cedd-120">App Service planı adı</span><span class="sxs-lookup"><span data-stu-id="3cedd-120">App Service Plan Name</span></span>

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

### <span data-ttu-id="3cedd-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3cedd-121">-ResourceGroupName</span></span>
<span data-ttu-id="3cedd-122">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="3cedd-122">Resource Group Name</span></span>

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

### <span data-ttu-id="3cedd-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="3cedd-123">-Confirm</span></span>
<span data-ttu-id="3cedd-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3cedd-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3cedd-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3cedd-125">-WhatIf</span></span>
<span data-ttu-id="3cedd-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3cedd-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3cedd-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3cedd-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3cedd-128">-Iş</span><span class="sxs-lookup"><span data-stu-id="3cedd-128">-AsJob</span></span>
<span data-ttu-id="3cedd-129">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="3cedd-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3cedd-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cedd-130">CommonParameters</span></span>
<span data-ttu-id="3cedd-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3cedd-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cedd-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3cedd-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cedd-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3cedd-133">INPUTS</span></span>

### <span data-ttu-id="3cedd-134">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="3cedd-134">ServerFarmWithRichSku</span></span>
<span data-ttu-id="3cedd-135">' AppServicePlan ' parametresi ardışık düzenin ' ServerFarmWithRichSku ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="3cedd-135">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="3cedd-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3cedd-136">OUTPUTS</span></span>

### <span data-ttu-id="3cedd-137">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="3cedd-137">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="3cedd-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3cedd-138">NOTES</span></span>

## <span data-ttu-id="3cedd-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3cedd-139">RELATED LINKS</span></span>

[<span data-ttu-id="3cedd-140">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="3cedd-140">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="3cedd-141">Yeni-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="3cedd-141">New-AzureRmAppServicePlan</span></span>](./New-AzureRmAppServicePlan.md)

[<span data-ttu-id="3cedd-142">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="3cedd-142">Set-AzureRmAppServicePlan</span></span>](./Set-AzureRmAppServicePlan.md)


