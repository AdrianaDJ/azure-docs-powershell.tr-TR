---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 56550997-21D9-4F85-B23A-677625482547
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/remove-azurermintegrationaccountschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountSchema.md
ms.openlocfilehash: 2600928a21548a4af49d3d7453b04cc2c505feb8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590902"
---
# <span data-ttu-id="01617-101">Remove-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="01617-101">Remove-AzureRmIntegrationAccountSchema</span></span>

## <span data-ttu-id="01617-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01617-102">SYNOPSIS</span></span>
<span data-ttu-id="01617-103">Tümleştirme hesabı şemasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="01617-103">Removes an integration account schema.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="01617-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="01617-104">SYNTAX</span></span>

```
Remove-AzureRmIntegrationAccountSchema -ResourceGroupName <String> -Name <String> -SchemaName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01617-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="01617-105">DESCRIPTION</span></span>
<span data-ttu-id="01617-106">**Remove-AzureRmIntegrationAccountSchema** cmdlet 'i, bir kaynak grubundan tümleştirme hesabı şemasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="01617-106">The **Remove-AzureRmIntegrationAccountSchema** cmdlet removes an integration account schema from a resource group.</span></span>
<span data-ttu-id="01617-107">Tümleştirme hesap adını, kaynak grubu adını ve şema adını belirtme.</span><span class="sxs-lookup"><span data-stu-id="01617-107">Specifying the integration account name, resource group name, and schema name.</span></span>
<span data-ttu-id="01617-108">Bu modül dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="01617-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="01617-109">Dinamik parametre kullanmak için, komuta bunu yazın.</span><span class="sxs-lookup"><span data-stu-id="01617-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="01617-110">Dinamik parametrelerin adlarını keşfetmek için, cmdlet adından sonra bir kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="01617-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="01617-111">Gerekli bir şablon parametresini atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="01617-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="01617-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="01617-112">EXAMPLES</span></span>

### <span data-ttu-id="01617-113">Örnek 1: Tümleştirme hesabı şemasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="01617-113">Example 1: Remove an integration account schema</span></span>
```
PS C:\>Remove-AzureRmIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -SchemaName "IntegrationAccountSchema43"
```

<span data-ttu-id="01617-114">Bu komut, IntegrationAccountSchema43 adlı bir tümleştirme hesabı şemasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="01617-114">This command removes an integration account schema named IntegrationAccountSchema43.</span></span>

## <span data-ttu-id="01617-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="01617-115">PARAMETERS</span></span>

### <span data-ttu-id="01617-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01617-116">-DefaultProfile</span></span>
<span data-ttu-id="01617-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="01617-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="01617-118">-Force</span><span class="sxs-lookup"><span data-stu-id="01617-118">-Force</span></span>
<span data-ttu-id="01617-119">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="01617-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="01617-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="01617-120">-Name</span></span>
<span data-ttu-id="01617-121">Tümleştirme hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="01617-121">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="01617-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01617-122">-ResourceGroupName</span></span>
<span data-ttu-id="01617-123">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="01617-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="01617-124">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="01617-124">-SchemaName</span></span>
<span data-ttu-id="01617-125">Tümleştirme hesabı şemasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="01617-125">Specifies the name of an integration account schema.</span></span>

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

### <span data-ttu-id="01617-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="01617-126">-Confirm</span></span>
<span data-ttu-id="01617-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="01617-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01617-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01617-128">-WhatIf</span></span>
<span data-ttu-id="01617-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="01617-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01617-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="01617-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01617-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01617-131">CommonParameters</span></span>
<span data-ttu-id="01617-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="01617-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01617-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01617-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01617-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="01617-134">INPUTS</span></span>

### <span data-ttu-id="01617-135">System. String</span><span class="sxs-lookup"><span data-stu-id="01617-135">System.String</span></span>

## <span data-ttu-id="01617-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="01617-136">OUTPUTS</span></span>

### <span data-ttu-id="01617-137">System. void</span><span class="sxs-lookup"><span data-stu-id="01617-137">System.Void</span></span>

## <span data-ttu-id="01617-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="01617-138">NOTES</span></span>

## <span data-ttu-id="01617-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="01617-139">RELATED LINKS</span></span>

[<span data-ttu-id="01617-140">Get-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="01617-140">Get-AzureRmIntegrationAccountSchema</span></span>](./Get-AzureRmIntegrationAccountSchema.md)

[<span data-ttu-id="01617-141">Yeni-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="01617-141">New-AzureRmIntegrationAccountSchema</span></span>](./New-AzureRmIntegrationAccountSchema.md)

[<span data-ttu-id="01617-142">Set-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="01617-142">Set-AzureRmIntegrationAccountSchema</span></span>](./Set-AzureRmIntegrationAccountSchema.md)


