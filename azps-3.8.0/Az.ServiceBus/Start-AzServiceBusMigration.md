---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/start-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Start-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Start-AzServiceBusMigration.md
ms.openlocfilehash: 0837532c6e708b4ff7d8cbee4f5ad231b4032347
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104305"
---
# <span data-ttu-id="00260-101">Start-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="00260-101">Start-AzServiceBusMigration</span></span>

## <span data-ttu-id="00260-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00260-102">SYNOPSIS</span></span>
<span data-ttu-id="00260-103">Yeni bir geçiş yapılandırması oluşturur ve varlıkları standarttan Premium ad alanlarına geçirmeye başlar</span><span class="sxs-lookup"><span data-stu-id="00260-103">Creates a new Migration configuration and starts migrating entities from Standard to Premium namespaces</span></span>

## <span data-ttu-id="00260-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="00260-104">SYNTAX</span></span>

```
Start-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-TargetNameSpace] <String>
 [-PostMigrationName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="00260-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="00260-105">DESCRIPTION</span></span>
<span data-ttu-id="00260-106">**Start-AzServiceBusMigration** cmdlet 'i yeni bir geçiş yapılandırması oluşturur ve varlıkları standarttan Premium ad alanlarına geçirmeye başlar</span><span class="sxs-lookup"><span data-stu-id="00260-106">The **Start-AzServiceBusMigration** cmdlet creates an new Migration configuration and starts migrating entities from Standard to Premium namespaces</span></span>

## <span data-ttu-id="00260-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="00260-107">EXAMPLES</span></span>

### <span data-ttu-id="00260-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="00260-108">Example 1</span></span>
```powershell
PS C:\> Start-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMigration -TargetNameSpace /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMigration -PostMigrationName TestingNamespaceStandardMigrationPostMigration

Name              : TestingNamespaceStandardMigration
Id                : /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespaceStandardMigration/migrationConfigurations/$default
Type              : Microsoft.ServiceBus/Namespaces/migrationconfigurations
ProvisioningState : Accepted
TargetNamespace   : /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMigration
PostMigrationName : TestingNamespaceStandardMigrationPostMigration
```

<span data-ttu-id="00260-109">' TestingNamespaceStandardMigration ' için ' TestingNamespacePremiumMigration ' ad alanlarına yeni bir geçiş yapılandırması oluşturur</span><span class="sxs-lookup"><span data-stu-id="00260-109">Creates a new migration configuration for 'TestingNamespaceStandardMigration' to 'TestingNamespacePremiumMigration' namespaces</span></span>

## <span data-ttu-id="00260-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="00260-110">PARAMETERS</span></span>

### <span data-ttu-id="00260-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="00260-111">-AsJob</span></span>
<span data-ttu-id="00260-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="00260-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="00260-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00260-113">-DefaultProfile</span></span>
<span data-ttu-id="00260-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="00260-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00260-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="00260-115">-Name</span></span>
<span data-ttu-id="00260-116">Standart ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="00260-116">Standard Namespace Name</span></span>

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

### <span data-ttu-id="00260-117">-PostMigrationName</span><span class="sxs-lookup"><span data-stu-id="00260-117">-PostMigrationName</span></span>
<span data-ttu-id="00260-118">Geçiş sırasında standart ad alanı için geçiş sonrası adı</span><span class="sxs-lookup"><span data-stu-id="00260-118">Post Migration Name for Standard Namespace in Migration</span></span>

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

### <span data-ttu-id="00260-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00260-119">-ResourceGroupName</span></span>
<span data-ttu-id="00260-120">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="00260-120">Resource Group Name</span></span>

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

### <span data-ttu-id="00260-121">-TargetNameSpace</span><span class="sxs-lookup"><span data-stu-id="00260-121">-TargetNameSpace</span></span>
<span data-ttu-id="00260-122">Premium ad alanı ARM kimliği</span><span class="sxs-lookup"><span data-stu-id="00260-122">Premium Namespace ARM Id</span></span>

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

### <span data-ttu-id="00260-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="00260-123">-Confirm</span></span>
<span data-ttu-id="00260-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="00260-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00260-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00260-125">-WhatIf</span></span>
<span data-ttu-id="00260-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="00260-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00260-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="00260-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00260-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00260-128">CommonParameters</span></span>
<span data-ttu-id="00260-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="00260-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00260-130">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00260-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00260-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="00260-131">INPUTS</span></span>

### <span data-ttu-id="00260-132">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="00260-132">None</span></span>

## <span data-ttu-id="00260-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="00260-133">OUTPUTS</span></span>

### <span data-ttu-id="00260-134">Microsoft. Azure. Commands. ServiceBus. model. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="00260-134">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="00260-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="00260-135">NOTES</span></span>

## <span data-ttu-id="00260-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="00260-136">RELATED LINKS</span></span>
