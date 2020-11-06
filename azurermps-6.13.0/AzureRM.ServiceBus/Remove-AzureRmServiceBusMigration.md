---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusMigration.md
ms.openlocfilehash: c378f6315f66b7149c1a8bb6d51ce806425065a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589335"
---
# <span data-ttu-id="74ddd-101">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="74ddd-101">Remove-AzureRmServiceBusMigration</span></span>

## <span data-ttu-id="74ddd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74ddd-102">SYNOPSIS</span></span>
<span data-ttu-id="74ddd-103">Cmdlet, Standard için geçiş yapılandırmasını Premium ad alanlarına siler</span><span class="sxs-lookup"><span data-stu-id="74ddd-103">Cmdlet deletes the Migration configuration for Standard to Premium namespaces</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="74ddd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="74ddd-104">SYNTAX</span></span>

### <span data-ttu-id="74ddd-105">MigrationConfigurationPropertiesSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="74ddd-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Remove-AzureRmServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74ddd-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="74ddd-106">NamespaceInputObjectSet</span></span>
```
Remove-AzureRmServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74ddd-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="74ddd-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzureRmServiceBusMigration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74ddd-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="74ddd-108">DESCRIPTION</span></span>
<span data-ttu-id="74ddd-109">**Remove-AzureRmServiceBusMigration** cmdlet 'i standart için Premium ad alanlarına geçiş yapılandırmasını siler</span><span class="sxs-lookup"><span data-stu-id="74ddd-109">The **Remove-AzureRmServiceBusMigration** cmdlet deletes the Migration configuration for Standard to Premium namespaces</span></span>

## <span data-ttu-id="74ddd-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="74ddd-110">EXAMPLES</span></span>

### <span data-ttu-id="74ddd-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="74ddd-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMirgation
```

<span data-ttu-id="74ddd-112">' Testingnamespacestandardir, ' geçiş yapılandırmasını siler</span><span class="sxs-lookup"><span data-stu-id="74ddd-112">Deletes the 'TestingNamespaceStandardMirgation' migration configuration</span></span>

## <span data-ttu-id="74ddd-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="74ddd-113">PARAMETERS</span></span>

### <span data-ttu-id="74ddd-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="74ddd-114">-AsJob</span></span>
<span data-ttu-id="74ddd-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="74ddd-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="74ddd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74ddd-116">-DefaultProfile</span></span>
<span data-ttu-id="74ddd-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="74ddd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74ddd-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="74ddd-118">-InputObject</span></span>
<span data-ttu-id="74ddd-119">Hizmet veri yolu geçiş standart ad alanı nesnesi</span><span class="sxs-lookup"><span data-stu-id="74ddd-119">Service Bus Migration Standard Namespace Object</span></span>

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

### <span data-ttu-id="74ddd-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="74ddd-120">-Name</span></span>
<span data-ttu-id="74ddd-121">Standart ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="74ddd-121">Standard Namespace Name</span></span>

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

### <span data-ttu-id="74ddd-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="74ddd-122">-PassThru</span></span>
<span data-ttu-id="74ddd-123">Komut başarılı olmuşsa, bunu belirtmek doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="74ddd-123">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="74ddd-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74ddd-124">-ResourceGroupName</span></span>
<span data-ttu-id="74ddd-125">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="74ddd-125">Resource Group Name</span></span>

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

### <span data-ttu-id="74ddd-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="74ddd-126">-ResourceId</span></span>
<span data-ttu-id="74ddd-127">Hizmet veri yolu geçiş standart ad alanı kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="74ddd-127">Service Bus Migration Standard Namespace Resource Id</span></span>

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

### <span data-ttu-id="74ddd-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="74ddd-128">-Confirm</span></span>
<span data-ttu-id="74ddd-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="74ddd-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74ddd-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74ddd-130">-WhatIf</span></span>
<span data-ttu-id="74ddd-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="74ddd-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74ddd-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="74ddd-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74ddd-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74ddd-133">CommonParameters</span></span>
<span data-ttu-id="74ddd-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="74ddd-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74ddd-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74ddd-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74ddd-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="74ddd-136">INPUTS</span></span>

### <span data-ttu-id="74ddd-137">Microsoft. Azure. Commands. ServiceBus. model. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="74ddd-137">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>
<span data-ttu-id="74ddd-138">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="74ddd-138">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="74ddd-139">System. String</span><span class="sxs-lookup"><span data-stu-id="74ddd-139">System.String</span></span>

## <span data-ttu-id="74ddd-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="74ddd-140">OUTPUTS</span></span>

### <span data-ttu-id="74ddd-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="74ddd-141">System.Boolean</span></span>

## <span data-ttu-id="74ddd-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="74ddd-142">NOTES</span></span>

## <span data-ttu-id="74ddd-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="74ddd-143">RELATED LINKS</span></span>
