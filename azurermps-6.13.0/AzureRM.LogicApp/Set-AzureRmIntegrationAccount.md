---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: F6D9EA59-BA61-4117-8771-9B190424BFF8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/set-azurermintegrationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccount.md
ms.openlocfilehash: c6f86d31f97ac0f4fcdbdd45c6bc111eda045800
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762604"
---
# <span data-ttu-id="719a2-101">Set-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="719a2-101">Set-AzureRmIntegrationAccount</span></span>

## <span data-ttu-id="719a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="719a2-102">SYNOPSIS</span></span>
<span data-ttu-id="719a2-103">Tümleştirme hesabını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="719a2-103">Modifies an integration account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="719a2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="719a2-104">SYNTAX</span></span>

```
Set-AzureRmIntegrationAccount -ResourceGroupName <String> -Name <String> [-Location <String>] [-Sku <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="719a2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="719a2-105">DESCRIPTION</span></span>
<span data-ttu-id="719a2-106">**Set-AzureRmIntegrationAccount** cmdlet 'i bir tümleştirme hesabını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="719a2-106">The **Set-AzureRmIntegrationAccount** cmdlet modifies an integration account.</span></span>
<span data-ttu-id="719a2-107">Bu cmdlet, tümleştirme hesabını temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="719a2-107">This cmdlet returns an object that represents the integration account.</span></span>
<span data-ttu-id="719a2-108">Bu modül dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="719a2-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="719a2-109">Dinamik parametre kullanmak için, komuta bunu yazın.</span><span class="sxs-lookup"><span data-stu-id="719a2-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="719a2-110">Dinamik parametrelerin adlarını keşfetmek için, cmdlet adından sonra bir kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="719a2-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="719a2-111">Gerekli bir şablon parametresini atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="719a2-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="719a2-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="719a2-112">EXAMPLES</span></span>

### <span data-ttu-id="719a2-113">Örnek 1: Tümleştirme hesabını değiştirme</span><span class="sxs-lookup"><span data-stu-id="719a2-113">Example 1: Modify an integration account</span></span>
```
PS C:\>Set-AzureRmIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -Sku "Free"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="719a2-114">Bu komut, belirtilen kaynak grubundaki IntegrationAccount31 adındaki bir tümleştirme hesabını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="719a2-114">This command modifies an integration account named IntegrationAccount31 in the specified resource group.</span></span>

## <span data-ttu-id="719a2-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="719a2-115">PARAMETERS</span></span>

### <span data-ttu-id="719a2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="719a2-116">-DefaultProfile</span></span>
<span data-ttu-id="719a2-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="719a2-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="719a2-118">-Force</span><span class="sxs-lookup"><span data-stu-id="719a2-118">-Force</span></span>
<span data-ttu-id="719a2-119">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="719a2-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="719a2-120">-Konum</span><span class="sxs-lookup"><span data-stu-id="719a2-120">-Location</span></span>
<span data-ttu-id="719a2-121">Tümleştirme hesabı için bir konum belirtir.</span><span class="sxs-lookup"><span data-stu-id="719a2-121">Specifies a location for the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="719a2-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="719a2-122">-Name</span></span>
<span data-ttu-id="719a2-123">Tümleştirme hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="719a2-123">Specifies the name of the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="719a2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="719a2-124">-ResourceGroupName</span></span>
<span data-ttu-id="719a2-125">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="719a2-125">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="719a2-126">-SKU</span><span class="sxs-lookup"><span data-stu-id="719a2-126">-Sku</span></span>
<span data-ttu-id="719a2-127">Tümleştirme hesabı için bir SKU adı belirtir.</span><span class="sxs-lookup"><span data-stu-id="719a2-127">Specifies a SKU name for the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="719a2-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="719a2-128">-Confirm</span></span>
<span data-ttu-id="719a2-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="719a2-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="719a2-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="719a2-130">-WhatIf</span></span>
<span data-ttu-id="719a2-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="719a2-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="719a2-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="719a2-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="719a2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="719a2-133">CommonParameters</span></span>
<span data-ttu-id="719a2-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="719a2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="719a2-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="719a2-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="719a2-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="719a2-136">INPUTS</span></span>

### <span data-ttu-id="719a2-137">System. String</span><span class="sxs-lookup"><span data-stu-id="719a2-137">System.String</span></span>

## <span data-ttu-id="719a2-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="719a2-138">OUTPUTS</span></span>

### <span data-ttu-id="719a2-139">Microsoft. Azure. Management. Logic. modeller. ıntegrationhesabı</span><span class="sxs-lookup"><span data-stu-id="719a2-139">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

## <span data-ttu-id="719a2-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="719a2-140">NOTES</span></span>

## <span data-ttu-id="719a2-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="719a2-141">RELATED LINKS</span></span>

[<span data-ttu-id="719a2-142">Get-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="719a2-142">Get-AzureRmIntegrationAccount</span></span>](./Get-AzureRmIntegrationAccount.md)

[<span data-ttu-id="719a2-143">Yeni-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="719a2-143">New-AzureRmIntegrationAccount</span></span>](./New-AzureRmIntegrationAccount.md)

[<span data-ttu-id="719a2-144">Remove-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="719a2-144">Remove-AzureRmIntegrationAccount</span></span>](./Remove-AzureRmIntegrationAccount.md)

