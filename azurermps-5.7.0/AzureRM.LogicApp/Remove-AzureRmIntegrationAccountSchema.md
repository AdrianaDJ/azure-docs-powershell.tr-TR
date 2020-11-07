---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 56550997-21D9-4F85-B23A-677625482547
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/remove-azurermintegrationaccountschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountSchema.md
ms.openlocfilehash: a1a34ca669b12ee815655531c33b6cdba519016c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764704"
---
# <span data-ttu-id="bac66-101">Remove-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="bac66-101">Remove-AzureRmIntegrationAccountSchema</span></span>

## <span data-ttu-id="bac66-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bac66-102">SYNOPSIS</span></span>
<span data-ttu-id="bac66-103">Tümleştirme hesabı şemasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="bac66-103">Removes an integration account schema.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bac66-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bac66-104">SYNTAX</span></span>

```
Remove-AzureRmIntegrationAccountSchema -ResourceGroupName <String> -Name <String> -SchemaName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bac66-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="bac66-105">DESCRIPTION</span></span>
<span data-ttu-id="bac66-106">**Remove-AzureRmIntegrationAccountSchema** cmdlet 'i, bir kaynak grubundan tümleştirme hesabı şemasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="bac66-106">The **Remove-AzureRmIntegrationAccountSchema** cmdlet removes an integration account schema from a resource group.</span></span>
<span data-ttu-id="bac66-107">Tümleştirme hesap adını, kaynak grubu adını ve şema adını belirtme.</span><span class="sxs-lookup"><span data-stu-id="bac66-107">Specifying the integration account name, resource group name, and schema name.</span></span>

<span data-ttu-id="bac66-108">Bu modül dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="bac66-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="bac66-109">Dinamik parametre kullanmak için, komuta bunu yazın.</span><span class="sxs-lookup"><span data-stu-id="bac66-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="bac66-110">Dinamik parametrelerin adlarını keşfetmek için, cmdlet adından sonra bir kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="bac66-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="bac66-111">Gerekli bir şablon parametresini atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="bac66-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="bac66-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bac66-112">EXAMPLES</span></span>

### <span data-ttu-id="bac66-113">Örnek 1: Tümleştirme hesabı şemasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="bac66-113">Example 1: Remove an integration account schema</span></span>
```
PS C:\>Remove-AzureRmIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -SchemaName "IntegrationAccountSchema43"
```

<span data-ttu-id="bac66-114">Bu komut, IntegrationAccountSchema43 adlı bir tümleştirme hesabı şemasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="bac66-114">This command removes an integration account schema named IntegrationAccountSchema43.</span></span>

## <span data-ttu-id="bac66-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bac66-115">PARAMETERS</span></span>

### <span data-ttu-id="bac66-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bac66-116">-DefaultProfile</span></span>
<span data-ttu-id="bac66-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="bac66-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bac66-118">-Force</span><span class="sxs-lookup"><span data-stu-id="bac66-118">-Force</span></span>
<span data-ttu-id="bac66-119">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="bac66-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="bac66-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="bac66-120">-Name</span></span>
<span data-ttu-id="bac66-121">Tümleştirme hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bac66-121">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="bac66-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bac66-122">-ResourceGroupName</span></span>
<span data-ttu-id="bac66-123">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bac66-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="bac66-124">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="bac66-124">-SchemaName</span></span>
<span data-ttu-id="bac66-125">Tümleştirme hesabı şemasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bac66-125">Specifies the name of an integration account schema.</span></span>

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

### <span data-ttu-id="bac66-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="bac66-126">-Confirm</span></span>
<span data-ttu-id="bac66-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bac66-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bac66-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bac66-128">-WhatIf</span></span>
<span data-ttu-id="bac66-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bac66-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bac66-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bac66-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bac66-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bac66-131">CommonParameters</span></span>
<span data-ttu-id="bac66-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bac66-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bac66-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bac66-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bac66-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bac66-134">INPUTS</span></span>

### <span data-ttu-id="bac66-135">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="bac66-135">None</span></span>
<span data-ttu-id="bac66-136">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="bac66-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bac66-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bac66-137">OUTPUTS</span></span>

## <span data-ttu-id="bac66-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bac66-138">NOTES</span></span>

## <span data-ttu-id="bac66-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bac66-139">RELATED LINKS</span></span>

[<span data-ttu-id="bac66-140">Get-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="bac66-140">Get-AzureRmIntegrationAccountSchema</span></span>](./Get-AzureRmIntegrationAccountSchema.md)

[<span data-ttu-id="bac66-141">Yeni-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="bac66-141">New-AzureRmIntegrationAccountSchema</span></span>](./New-AzureRmIntegrationAccountSchema.md)

[<span data-ttu-id="bac66-142">Set-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="bac66-142">Set-AzureRmIntegrationAccountSchema</span></span>](./Set-AzureRmIntegrationAccountSchema.md)


