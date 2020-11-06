---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 7AAF2ACC-84ED-449C-B1E8-F074463F44EB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/remove-azurermintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountMap.md
ms.openlocfilehash: 769a92f9cd164ef2b3754a84d7a948f3bedd05da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588194"
---
# <span data-ttu-id="16dbc-101">Remove-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="16dbc-101">Remove-AzureRmIntegrationAccountMap</span></span>

## <span data-ttu-id="16dbc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16dbc-102">SYNOPSIS</span></span>
<span data-ttu-id="16dbc-103">Tümleştirme hesabı haritasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="16dbc-103">Removes an integration account map.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="16dbc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="16dbc-104">SYNTAX</span></span>

```
Remove-AzureRmIntegrationAccountMap -ResourceGroupName <String> -Name <String> -MapName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16dbc-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="16dbc-105">DESCRIPTION</span></span>
<span data-ttu-id="16dbc-106">**Remove-AzureRmIntegrationAccountMap** cmdlet 'i, bir kaynak grubundan tümleştirme hesabı haritasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="16dbc-106">The **Remove-AzureRmIntegrationAccountMap** cmdlet removes an integration account map from a resource group.</span></span>
<span data-ttu-id="16dbc-107">Tümleştirme hesap adını, kaynak grubu adını ve harita adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="16dbc-107">Specify the integration account name, resource group name, and map name.</span></span>

<span data-ttu-id="16dbc-108">Bu modül dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="16dbc-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="16dbc-109">Dinamik parametre kullanmak için, komuta bunu yazın.</span><span class="sxs-lookup"><span data-stu-id="16dbc-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="16dbc-110">Dinamik parametrelerin adlarını keşfetmek için, cmdlet adından sonra bir kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="16dbc-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="16dbc-111">Gerekli bir şablon parametresini atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="16dbc-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="16dbc-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="16dbc-112">EXAMPLES</span></span>

### <span data-ttu-id="16dbc-113">Örnek 1: Tümleştirme hesabı haritasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="16dbc-113">Example 1: Remove an integration account map</span></span>
```
PS C:\>Remove-AzureRmIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47"
```

<span data-ttu-id="16dbc-114">Bu komut, IntegrationAccountMap47 adlı tümleştirme hesabı haritasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="16dbc-114">This command removes the integration account map named IntegrationAccountMap47.</span></span>

## <span data-ttu-id="16dbc-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="16dbc-115">PARAMETERS</span></span>

### <span data-ttu-id="16dbc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16dbc-116">-DefaultProfile</span></span>
<span data-ttu-id="16dbc-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="16dbc-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="16dbc-118">-Force</span><span class="sxs-lookup"><span data-stu-id="16dbc-118">-Force</span></span>
<span data-ttu-id="16dbc-119">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="16dbc-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="16dbc-120">-MapName</span><span class="sxs-lookup"><span data-stu-id="16dbc-120">-MapName</span></span>
<span data-ttu-id="16dbc-121">Tümleştirme hesabı eşlemesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="16dbc-121">Specifies the name of the integration account map.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16dbc-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="16dbc-122">-Name</span></span>
<span data-ttu-id="16dbc-123">Tümleştirme hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="16dbc-123">Specifies the name of the integration account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16dbc-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16dbc-124">-ResourceGroupName</span></span>
<span data-ttu-id="16dbc-125">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="16dbc-125">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16dbc-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="16dbc-126">-Confirm</span></span>
<span data-ttu-id="16dbc-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="16dbc-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16dbc-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16dbc-128">-WhatIf</span></span>
<span data-ttu-id="16dbc-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="16dbc-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16dbc-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="16dbc-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16dbc-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16dbc-131">CommonParameters</span></span>
<span data-ttu-id="16dbc-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="16dbc-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16dbc-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16dbc-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16dbc-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="16dbc-134">INPUTS</span></span>

### <span data-ttu-id="16dbc-135">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="16dbc-135">None</span></span>
<span data-ttu-id="16dbc-136">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="16dbc-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="16dbc-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="16dbc-137">OUTPUTS</span></span>

## <span data-ttu-id="16dbc-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="16dbc-138">NOTES</span></span>

## <span data-ttu-id="16dbc-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="16dbc-139">RELATED LINKS</span></span>

[<span data-ttu-id="16dbc-140">Get-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="16dbc-140">Get-AzureRmIntegrationAccountMap</span></span>](./Get-AzureRmIntegrationAccountMap.md)

[<span data-ttu-id="16dbc-141">Yeni-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="16dbc-141">New-AzureRmIntegrationAccountMap</span></span>](./New-AzureRmIntegrationAccountMap.md)

[<span data-ttu-id="16dbc-142">Set-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="16dbc-142">Set-AzureRmIntegrationAccountMap</span></span>](./Set-AzureRmIntegrationAccountMap.md)


