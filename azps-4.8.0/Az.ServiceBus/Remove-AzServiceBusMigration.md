---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusMigration.md
ms.openlocfilehash: 42bb6a61e2298c43cb0828a031495b086b46c9d2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267631"
---
# <span data-ttu-id="b1a2c-101">Remove-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="b1a2c-101">Remove-AzServiceBusMigration</span></span>

## <span data-ttu-id="b1a2c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1a2c-102">SYNOPSIS</span></span>
<span data-ttu-id="b1a2c-103">Cmdlet, Standard için geçiş yapılandırmasını Premium ad alanlarına siler</span><span class="sxs-lookup"><span data-stu-id="b1a2c-103">Cmdlet deletes the Migration configuration for Standard to Premium namespaces</span></span>

## <span data-ttu-id="b1a2c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b1a2c-104">SYNTAX</span></span>

### <span data-ttu-id="b1a2c-105">MigrationConfigurationPropertiesSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b1a2c-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1a2c-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b1a2c-106">NamespaceInputObjectSet</span></span>
```
Remove-AzServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1a2c-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1a2c-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzServiceBusMigration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1a2c-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="b1a2c-108">DESCRIPTION</span></span>
<span data-ttu-id="b1a2c-109">**Remove-AzServiceBusMigration** cmdlet 'i standart için Premium ad alanlarına geçiş yapılandırmasını siler</span><span class="sxs-lookup"><span data-stu-id="b1a2c-109">The **Remove-AzServiceBusMigration** cmdlet deletes the Migration configuration for Standard to Premium namespaces</span></span>

## <span data-ttu-id="b1a2c-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b1a2c-110">EXAMPLES</span></span>

### <span data-ttu-id="b1a2c-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b1a2c-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMigration
```

<span data-ttu-id="b1a2c-112">' TestingNamespaceStandardMigration ' geçiş yapılandırmasını siler</span><span class="sxs-lookup"><span data-stu-id="b1a2c-112">Deletes the 'TestingNamespaceStandardMigration' migration configuration</span></span>

## <span data-ttu-id="b1a2c-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b1a2c-113">PARAMETERS</span></span>

### <span data-ttu-id="b1a2c-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="b1a2c-114">-AsJob</span></span>
<span data-ttu-id="b1a2c-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="b1a2c-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b1a2c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1a2c-116">-DefaultProfile</span></span>
<span data-ttu-id="b1a2c-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b1a2c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1a2c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b1a2c-118">-InputObject</span></span>
<span data-ttu-id="b1a2c-119">Hizmet veri yolu geçiş standart ad alanı nesnesi</span><span class="sxs-lookup"><span data-stu-id="b1a2c-119">Service Bus Migration Standard Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b1a2c-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="b1a2c-120">-Name</span></span>
<span data-ttu-id="b1a2c-121">Standart ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="b1a2c-121">Standard Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: MigrationConfigurationPropertiesSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1a2c-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="b1a2c-122">-PassThru</span></span>
<span data-ttu-id="b1a2c-123">Komut başarılı olmuşsa, bunu belirtmek doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="b1a2c-123">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="b1a2c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1a2c-124">-ResourceGroupName</span></span>
<span data-ttu-id="b1a2c-125">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="b1a2c-125">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: MigrationConfigurationPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1a2c-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="b1a2c-126">-ResourceId</span></span>
<span data-ttu-id="b1a2c-127">Hizmet veri yolu geçiş standart ad alanı kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="b1a2c-127">Service Bus Migration Standard Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1a2c-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="b1a2c-128">-Confirm</span></span>
<span data-ttu-id="b1a2c-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b1a2c-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1a2c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1a2c-130">-WhatIf</span></span>
<span data-ttu-id="b1a2c-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b1a2c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1a2c-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b1a2c-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1a2c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1a2c-133">CommonParameters</span></span>
<span data-ttu-id="b1a2c-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b1a2c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1a2c-135">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1a2c-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1a2c-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b1a2c-136">INPUTS</span></span>

### <span data-ttu-id="b1a2c-137">Microsoft. Azure. Commands. ServiceBus. model. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="b1a2c-137">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

### <span data-ttu-id="b1a2c-138">System. String</span><span class="sxs-lookup"><span data-stu-id="b1a2c-138">System.String</span></span>

## <span data-ttu-id="b1a2c-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b1a2c-139">OUTPUTS</span></span>

### <span data-ttu-id="b1a2c-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b1a2c-140">System.Boolean</span></span>

## <span data-ttu-id="b1a2c-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b1a2c-141">NOTES</span></span>

## <span data-ttu-id="b1a2c-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b1a2c-142">RELATED LINKS</span></span>
