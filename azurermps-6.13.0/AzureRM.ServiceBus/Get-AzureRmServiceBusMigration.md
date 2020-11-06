---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusMigration.md
ms.openlocfilehash: cdf869f13c90982c40568f37c0757ef2e7547b3c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590867"
---
# <span data-ttu-id="b3e7f-101">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="b3e7f-101">Get-AzureRmServiceBusMigration</span></span>

## <span data-ttu-id="b3e7f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3e7f-102">SYNOPSIS</span></span>
<span data-ttu-id="b3e7f-103">Ad alanı için MigrationConfiguration 'ı getirir</span><span class="sxs-lookup"><span data-stu-id="b3e7f-103">Retrieves MigrationConfiguration for the namespace</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b3e7f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b3e7f-104">SYNTAX</span></span>

### <span data-ttu-id="b3e7f-105">MigrationConfigurationPropertiesSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b3e7f-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Get-AzureRmServiceBusMigration [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3e7f-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b3e7f-106">NamespaceInputObjectSet</span></span>
```
Get-AzureRmServiceBusMigration [-InputObject] <PSNamespaceAttributes>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3e7f-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="b3e7f-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmServiceBusMigration [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b3e7f-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="b3e7f-108">DESCRIPTION</span></span>
<span data-ttu-id="b3e7f-109">**Get-AzureRmServiceBusMigration** , ad alanı Için geçiş yapılandırmasını alır</span><span class="sxs-lookup"><span data-stu-id="b3e7f-109">The **Get-AzureRmServiceBusMigration** Retrieves Migration Configuration for the namespace</span></span>

## <span data-ttu-id="b3e7f-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b3e7f-110">EXAMPLES</span></span>

### <span data-ttu-id="b3e7f-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b3e7f-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMirgation

Name              : TestingNamespaceStandardMirgation
Id                : /subscriptions/d7670b40-0217-4af9-985c-972f6702782e/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespaceStandardMirgation/migrationConfigurations/$default
Type              : Microsoft.ServiceBus/Namespaces/migrationconfigurations
ProvisioningState : Succeeded
PendingReplicationOperationsCount : 40
TargetNamespace   : /subscriptions/d7670b40-0217-4af9-985c-972f6702782e/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMirgation
PostMigrationName : TestingNamespaceStandardMirgationPostMigration
```

<span data-ttu-id="b3e7f-112">' Testingnamespacestandardir, ' öğesinin geçiş yapılandırma özelliklerini alır</span><span class="sxs-lookup"><span data-stu-id="b3e7f-112">Gets the Migration Configuration properties of 'TestingNamespaceStandardMirgation'</span></span>

## <span data-ttu-id="b3e7f-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b3e7f-113">PARAMETERS</span></span>

### <span data-ttu-id="b3e7f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3e7f-114">-DefaultProfile</span></span>
<span data-ttu-id="b3e7f-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b3e7f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3e7f-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b3e7f-116">-InputObject</span></span>
<span data-ttu-id="b3e7f-117">Namespace nesnesi</span><span class="sxs-lookup"><span data-stu-id="b3e7f-117">Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b3e7f-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="b3e7f-118">-Name</span></span>
<span data-ttu-id="b3e7f-119">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="b3e7f-119">Namespace Name</span></span>

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

### <span data-ttu-id="b3e7f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3e7f-120">-ResourceGroupName</span></span>
<span data-ttu-id="b3e7f-121">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="b3e7f-121">Resource Group Name</span></span>

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

### <span data-ttu-id="b3e7f-122">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="b3e7f-122">-ResourceId</span></span>
<span data-ttu-id="b3e7f-123">Ad alanı kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="b3e7f-123">Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3e7f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3e7f-124">CommonParameters</span></span>
<span data-ttu-id="b3e7f-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b3e7f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3e7f-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3e7f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3e7f-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b3e7f-127">INPUTS</span></span>

### <span data-ttu-id="b3e7f-128">Microsoft. Azure. Commands. ServiceBus. modeller. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="b3e7f-128">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>
<span data-ttu-id="b3e7f-129">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b3e7f-129">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="b3e7f-130">System. String</span><span class="sxs-lookup"><span data-stu-id="b3e7f-130">System.String</span></span>

## <span data-ttu-id="b3e7f-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b3e7f-131">OUTPUTS</span></span>

### <span data-ttu-id="b3e7f-132">Microsoft. Azure. Commands. ServiceBus. modeller. PSServiceBusMigrationConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="b3e7f-132">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusMigrationConfigurationAttributes</span></span>

## <span data-ttu-id="b3e7f-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b3e7f-133">NOTES</span></span>

## <span data-ttu-id="b3e7f-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b3e7f-134">RELATED LINKS</span></span>
