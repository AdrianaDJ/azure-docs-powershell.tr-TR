---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 5F1A4FE0-CB57-45D3-9F08-879469A61E1E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/new-azurermintegrationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccount.md
ms.openlocfilehash: 7183078623c3be1826c98712fa41524643a4a68c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590909"
---
# <span data-ttu-id="8d65d-101">New-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="8d65d-101">New-AzureRmIntegrationAccount</span></span>

## <span data-ttu-id="8d65d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d65d-102">SYNOPSIS</span></span>
<span data-ttu-id="8d65d-103">Tümleştirme hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8d65d-103">Creates an integration account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8d65d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8d65d-104">SYNTAX</span></span>

```
New-AzureRmIntegrationAccount -ResourceGroupName <String> -Name <String> -Location <String> [-Sku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d65d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8d65d-105">DESCRIPTION</span></span>
<span data-ttu-id="8d65d-106">**Yeni-AzureRmIntegrationAccount** cmdlet 'i bir tümleştirme hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8d65d-106">The **New-AzureRmIntegrationAccount** cmdlet creates an integration account.</span></span>
<span data-ttu-id="8d65d-107">Bu cmdlet, tümleştirme hesabını temsil eden bir nesne döndürür. Bir ad, konum, kaynak grubu adı ve SKU adı belirtin.</span><span class="sxs-lookup"><span data-stu-id="8d65d-107">This cmdlet returns an object that represents the integration account.Specify a name, location, resource group name, and SKU name.</span></span>
<span data-ttu-id="8d65d-108">Komut satırında belirttiğiniz şablon parametre dosyası değerleri, bir şablon parametre nesnesindeki şablon parametre değerlerinden önceliklidir.</span><span class="sxs-lookup"><span data-stu-id="8d65d-108">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="8d65d-109">Bu modül dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="8d65d-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="8d65d-110">Dinamik parametre kullanmak için, komuta bunu yazın.</span><span class="sxs-lookup"><span data-stu-id="8d65d-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="8d65d-111">Dinamik parametrelerin adlarını keşfetmek için, cmdlet adından sonra bir kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="8d65d-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="8d65d-112">Gerekli bir şablon parametresini atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="8d65d-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="8d65d-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8d65d-113">EXAMPLES</span></span>

### <span data-ttu-id="8d65d-114">Örnek 1: Tümleştirme hesabı oluşturma</span><span class="sxs-lookup"><span data-stu-id="8d65d-114">Example 1: Create an integration account</span></span>
```
PS C:\>New-AzureRmIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -Location "brazilsouth" -Sku "Standard"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="8d65d-115">Bu komut, belirtilen kaynak grubunda IntegrationAccount31 adlı bir tümleştirme hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8d65d-115">This command creates an integration account named IntegrationAccount31 in the specified resource group.</span></span>

## <span data-ttu-id="8d65d-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8d65d-116">PARAMETERS</span></span>

### <span data-ttu-id="8d65d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d65d-117">-DefaultProfile</span></span>
<span data-ttu-id="8d65d-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="8d65d-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8d65d-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="8d65d-119">-Location</span></span>
<span data-ttu-id="8d65d-120">Tümleştirme hesabı için bir konum belirtir.</span><span class="sxs-lookup"><span data-stu-id="8d65d-120">Specifies a location for the integration account.</span></span>

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

### <span data-ttu-id="8d65d-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="8d65d-121">-Name</span></span>
<span data-ttu-id="8d65d-122">Tümleştirme hesabı için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="8d65d-122">Specifies a name for the integration account.</span></span>

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

### <span data-ttu-id="8d65d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d65d-123">-ResourceGroupName</span></span>
<span data-ttu-id="8d65d-124">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8d65d-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="8d65d-125">-SKU</span><span class="sxs-lookup"><span data-stu-id="8d65d-125">-Sku</span></span>
<span data-ttu-id="8d65d-126">Tümleştirme hesabı için bir SKU adı belirtir.</span><span class="sxs-lookup"><span data-stu-id="8d65d-126">Specifies a SKU name for the integration account.</span></span>

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

### <span data-ttu-id="8d65d-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="8d65d-127">-Confirm</span></span>
<span data-ttu-id="8d65d-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8d65d-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d65d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d65d-129">-WhatIf</span></span>
<span data-ttu-id="8d65d-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8d65d-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d65d-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8d65d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d65d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d65d-132">CommonParameters</span></span>
<span data-ttu-id="8d65d-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8d65d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d65d-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d65d-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d65d-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8d65d-135">INPUTS</span></span>

### <span data-ttu-id="8d65d-136">System. String</span><span class="sxs-lookup"><span data-stu-id="8d65d-136">System.String</span></span>

## <span data-ttu-id="8d65d-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8d65d-137">OUTPUTS</span></span>

### <span data-ttu-id="8d65d-138">Microsoft. Azure. Management. Logic. modeller. ıntegrationhesabı</span><span class="sxs-lookup"><span data-stu-id="8d65d-138">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

## <span data-ttu-id="8d65d-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8d65d-139">NOTES</span></span>

## <span data-ttu-id="8d65d-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8d65d-140">RELATED LINKS</span></span>

[<span data-ttu-id="8d65d-141">Get-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="8d65d-141">Get-AzureRmIntegrationAccount</span></span>](./Get-AzureRmIntegrationAccount.md)

[<span data-ttu-id="8d65d-142">Remove-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="8d65d-142">Remove-AzureRmIntegrationAccount</span></span>](./Remove-AzureRmIntegrationAccount.md)

[<span data-ttu-id="8d65d-143">Set-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="8d65d-143">Set-AzureRmIntegrationAccount</span></span>](./Set-AzureRmIntegrationAccount.md)

