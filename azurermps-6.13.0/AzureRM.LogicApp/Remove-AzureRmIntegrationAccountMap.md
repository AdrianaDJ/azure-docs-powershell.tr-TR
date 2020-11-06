---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 7AAF2ACC-84ED-449C-B1E8-F074463F44EB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/remove-azurermintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountMap.md
ms.openlocfilehash: db3ff812c1c774feb07dd8ec688381cd29fa5cd2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590906"
---
# <span data-ttu-id="d72be-101">Remove-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="d72be-101">Remove-AzureRmIntegrationAccountMap</span></span>

## <span data-ttu-id="d72be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d72be-102">SYNOPSIS</span></span>
<span data-ttu-id="d72be-103">Tümleştirme hesabı haritasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d72be-103">Removes an integration account map.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d72be-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d72be-104">SYNTAX</span></span>

```
Remove-AzureRmIntegrationAccountMap -ResourceGroupName <String> -Name <String> -MapName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d72be-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d72be-105">DESCRIPTION</span></span>
<span data-ttu-id="d72be-106">**Remove-AzureRmIntegrationAccountMap** cmdlet 'i, bir kaynak grubundan tümleştirme hesabı haritasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d72be-106">The **Remove-AzureRmIntegrationAccountMap** cmdlet removes an integration account map from a resource group.</span></span>
<span data-ttu-id="d72be-107">Tümleştirme hesap adını, kaynak grubu adını ve harita adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="d72be-107">Specify the integration account name, resource group name, and map name.</span></span>
<span data-ttu-id="d72be-108">Bu modül dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="d72be-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="d72be-109">Dinamik parametre kullanmak için, komuta bunu yazın.</span><span class="sxs-lookup"><span data-stu-id="d72be-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="d72be-110">Dinamik parametrelerin adlarını keşfetmek için, cmdlet adından sonra bir kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="d72be-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="d72be-111">Gerekli bir şablon parametresini atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="d72be-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="d72be-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d72be-112">EXAMPLES</span></span>

### <span data-ttu-id="d72be-113">Örnek 1: Tümleştirme hesabı haritasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="d72be-113">Example 1: Remove an integration account map</span></span>
```
PS C:\>Remove-AzureRmIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47"
```

<span data-ttu-id="d72be-114">Bu komut, IntegrationAccountMap47 adlı tümleştirme hesabı haritasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d72be-114">This command removes the integration account map named IntegrationAccountMap47.</span></span>

## <span data-ttu-id="d72be-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d72be-115">PARAMETERS</span></span>

### <span data-ttu-id="d72be-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d72be-116">-DefaultProfile</span></span>
<span data-ttu-id="d72be-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="d72be-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d72be-118">-Force</span><span class="sxs-lookup"><span data-stu-id="d72be-118">-Force</span></span>
<span data-ttu-id="d72be-119">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="d72be-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d72be-120">-MapName</span><span class="sxs-lookup"><span data-stu-id="d72be-120">-MapName</span></span>
<span data-ttu-id="d72be-121">Tümleştirme hesabı eşlemesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d72be-121">Specifies the name of the integration account map.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d72be-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="d72be-122">-Name</span></span>
<span data-ttu-id="d72be-123">Tümleştirme hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d72be-123">Specifies the name of the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d72be-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d72be-124">-ResourceGroupName</span></span>
<span data-ttu-id="d72be-125">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d72be-125">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d72be-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="d72be-126">-Confirm</span></span>
<span data-ttu-id="d72be-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d72be-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d72be-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d72be-128">-WhatIf</span></span>
<span data-ttu-id="d72be-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d72be-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d72be-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d72be-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d72be-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d72be-131">CommonParameters</span></span>
<span data-ttu-id="d72be-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d72be-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d72be-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d72be-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d72be-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d72be-134">INPUTS</span></span>

### <span data-ttu-id="d72be-135">System. String</span><span class="sxs-lookup"><span data-stu-id="d72be-135">System.String</span></span>

## <span data-ttu-id="d72be-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d72be-136">OUTPUTS</span></span>

### <span data-ttu-id="d72be-137">System. void</span><span class="sxs-lookup"><span data-stu-id="d72be-137">System.Void</span></span>

## <span data-ttu-id="d72be-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d72be-138">NOTES</span></span>

## <span data-ttu-id="d72be-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d72be-139">RELATED LINKS</span></span>

[<span data-ttu-id="d72be-140">Get-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="d72be-140">Get-AzureRmIntegrationAccountMap</span></span>](./Get-AzureRmIntegrationAccountMap.md)

[<span data-ttu-id="d72be-141">Yeni-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="d72be-141">New-AzureRmIntegrationAccountMap</span></span>](./New-AzureRmIntegrationAccountMap.md)

[<span data-ttu-id="d72be-142">Set-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="d72be-142">Set-AzureRmIntegrationAccountMap</span></span>](./Set-AzureRmIntegrationAccountMap.md)


