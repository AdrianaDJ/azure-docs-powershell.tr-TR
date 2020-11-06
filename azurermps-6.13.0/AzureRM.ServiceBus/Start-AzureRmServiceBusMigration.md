---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/start-azurermservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Start-AzureRmServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Start-AzureRmServiceBusMigration.md
ms.openlocfilehash: 979db64fb11b4fffc901d96811b24be5c79f6b63
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590859"
---
# <span data-ttu-id="e1c90-101">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="e1c90-101">Start-AzureRmServiceBusMigration</span></span>

## <span data-ttu-id="e1c90-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1c90-102">SYNOPSIS</span></span>
<span data-ttu-id="e1c90-103">Yeni bir geçiş yapılandırması oluşturur ve varlıkları standarttan Premium ad alanlarına geçirmeye başlar</span><span class="sxs-lookup"><span data-stu-id="e1c90-103">Creates a new Migration configuration and starts migrating entities from Standard to Premium namespaces</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e1c90-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e1c90-104">SYNTAX</span></span>

```
Start-AzureRmServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-TargetNameSpace] <String>
 [-PostMigrationName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e1c90-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e1c90-105">DESCRIPTION</span></span>
<span data-ttu-id="e1c90-106">**Start-AzureRmServiceBusMigration** cmdlet 'i yeni bir geçiş yapılandırması oluşturur ve varlıkları standarttan Premium ad alanlarına geçirmeye başlar</span><span class="sxs-lookup"><span data-stu-id="e1c90-106">The **Start-AzureRmServiceBusMigration** cmdlet creates an new Migration configuration and starts migrating entities from Standard to Premium namespaces</span></span>

## <span data-ttu-id="e1c90-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e1c90-107">EXAMPLES</span></span>

### <span data-ttu-id="e1c90-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e1c90-108">Example 1</span></span>
```powershell
PS C:\> Start-AzureRmServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMirgation -TargetNameSpace /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMirgation -PostMigrationName TestingNamespaceStandardMirgationPostMigration

Name              : TestingNamespaceStandardMirgation
Id                : /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespaceStandardMirgation/migrationConfigurations/$default
Type              : Microsoft.ServiceBus/Namespaces/migrationconfigurations
ProvisioningState : Accepted
TargetNamespace   : /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMirgation
PostMigrationName : TestingNamespaceStandardMirgationPostMigration
```

<span data-ttu-id="e1c90-109">' Testingnamespacestandardmirınyer ad alanları için yeni bir geçiş yapılandırması oluşturur</span><span class="sxs-lookup"><span data-stu-id="e1c90-109">Creates a new migration configuration for 'TestingNamespaceStandardMirgation' to 'TestingNamespacePremiumMirgation' namespaces</span></span>

## <span data-ttu-id="e1c90-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e1c90-110">PARAMETERS</span></span>

### <span data-ttu-id="e1c90-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="e1c90-111">-AsJob</span></span>
<span data-ttu-id="e1c90-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="e1c90-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e1c90-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1c90-113">-DefaultProfile</span></span>
<span data-ttu-id="e1c90-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e1c90-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1c90-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="e1c90-115">-Name</span></span>
<span data-ttu-id="e1c90-116">Standart ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="e1c90-116">Standard Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1c90-117">-PostMigrationName</span><span class="sxs-lookup"><span data-stu-id="e1c90-117">-PostMigrationName</span></span>
<span data-ttu-id="e1c90-118">Geçiş için,</span><span class="sxs-lookup"><span data-stu-id="e1c90-118">Post Migration Name for Standrad Namespace in Migration</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1c90-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1c90-119">-ResourceGroupName</span></span>
<span data-ttu-id="e1c90-120">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="e1c90-120">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1c90-121">-TargetNameSpace</span><span class="sxs-lookup"><span data-stu-id="e1c90-121">-TargetNameSpace</span></span>
<span data-ttu-id="e1c90-122">Premium ad alanı ARM kimliği</span><span class="sxs-lookup"><span data-stu-id="e1c90-122">Premium Namespace ARM Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1c90-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="e1c90-123">-Confirm</span></span>
<span data-ttu-id="e1c90-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e1c90-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1c90-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1c90-125">-WhatIf</span></span>
<span data-ttu-id="e1c90-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e1c90-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1c90-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e1c90-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1c90-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1c90-128">CommonParameters</span></span>
<span data-ttu-id="e1c90-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e1c90-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1c90-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1c90-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1c90-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e1c90-131">INPUTS</span></span>

### <span data-ttu-id="e1c90-132">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="e1c90-132">None</span></span>

## <span data-ttu-id="e1c90-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e1c90-133">OUTPUTS</span></span>

### <span data-ttu-id="e1c90-134">Microsoft. Azure. Commands. ServiceBus. model. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="e1c90-134">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="e1c90-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e1c90-135">NOTES</span></span>

## <span data-ttu-id="e1c90-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e1c90-136">RELATED LINKS</span></span>
