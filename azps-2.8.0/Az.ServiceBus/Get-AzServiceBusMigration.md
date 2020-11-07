---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusMigration.md
ms.openlocfilehash: 1e782c381ec10d03f269fc0a2d0871f064e4ddef
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932481"
---
# <span data-ttu-id="dd5ee-101">Get-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="dd5ee-101">Get-AzServiceBusMigration</span></span>

## <span data-ttu-id="dd5ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd5ee-102">SYNOPSIS</span></span>
<span data-ttu-id="dd5ee-103">Ad alanı için MigrationConfiguration 'ı getirir</span><span class="sxs-lookup"><span data-stu-id="dd5ee-103">Retrieves MigrationConfiguration for the namespace</span></span>

## <span data-ttu-id="dd5ee-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dd5ee-104">SYNTAX</span></span>

### <span data-ttu-id="dd5ee-105">MigrationConfigurationPropertiesSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="dd5ee-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Get-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dd5ee-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="dd5ee-106">NamespaceInputObjectSet</span></span>
```
Get-AzServiceBusMigration [-InputObject] <PSNamespaceAttributes> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dd5ee-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="dd5ee-107">ResourceIdParameterSet</span></span>
```
Get-AzServiceBusMigration [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dd5ee-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="dd5ee-108">DESCRIPTION</span></span>
<span data-ttu-id="dd5ee-109">**Get-AzServiceBusMigration** , ad alanı Için geçiş yapılandırmasını alır</span><span class="sxs-lookup"><span data-stu-id="dd5ee-109">The **Get-AzServiceBusMigration** Retrieves Migration Configuration for the namespace</span></span>

## <span data-ttu-id="dd5ee-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dd5ee-110">EXAMPLES</span></span>

### <span data-ttu-id="dd5ee-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="dd5ee-111">Example 1</span></span>
```powershell
PS C:\> Get-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMigration

Name              : TestingNamespaceStandardMigration
Id                : /subscriptions/d7670b40-0217-4af9-985c-972f6702782e/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespaceStandardMigration/migrationConfigurations/$default
Type              : Microsoft.ServiceBus/Namespaces/migrationconfigurations
ProvisioningState : Succeeded
PendingReplicationOperationsCount : 40
TargetNamespace   : /subscriptions/d7670b40-0217-4af9-985c-972f6702782e/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMigration
PostMigrationName : TestingNamespaceStandardMigrationPostMigration
```

<span data-ttu-id="dd5ee-112">' TestingNamespaceStandardMigration ' öğesinin geçiş yapılandırma özelliklerini alır</span><span class="sxs-lookup"><span data-stu-id="dd5ee-112">Gets the Migration Configuration properties of 'TestingNamespaceStandardMigration'</span></span>

## <span data-ttu-id="dd5ee-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dd5ee-113">PARAMETERS</span></span>

### <span data-ttu-id="dd5ee-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd5ee-114">-DefaultProfile</span></span>
<span data-ttu-id="dd5ee-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dd5ee-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd5ee-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dd5ee-116">-InputObject</span></span>
<span data-ttu-id="dd5ee-117">Namespace nesnesi</span><span class="sxs-lookup"><span data-stu-id="dd5ee-117">Namespace Object</span></span>

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

### <span data-ttu-id="dd5ee-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="dd5ee-118">-Name</span></span>
<span data-ttu-id="dd5ee-119">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="dd5ee-119">Namespace Name</span></span>

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

### <span data-ttu-id="dd5ee-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd5ee-120">-ResourceGroupName</span></span>
<span data-ttu-id="dd5ee-121">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="dd5ee-121">Resource Group Name</span></span>

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

### <span data-ttu-id="dd5ee-122">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="dd5ee-122">-ResourceId</span></span>
<span data-ttu-id="dd5ee-123">Ad alanı kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="dd5ee-123">Namespace Resource Id</span></span>

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

### <span data-ttu-id="dd5ee-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd5ee-124">CommonParameters</span></span>
<span data-ttu-id="dd5ee-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dd5ee-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd5ee-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd5ee-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd5ee-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dd5ee-127">INPUTS</span></span>

### <span data-ttu-id="dd5ee-128">Microsoft. Azure. Commands. ServiceBus. modeller. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="dd5ee-128">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

### <span data-ttu-id="dd5ee-129">System. String</span><span class="sxs-lookup"><span data-stu-id="dd5ee-129">System.String</span></span>

## <span data-ttu-id="dd5ee-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dd5ee-130">OUTPUTS</span></span>

### <span data-ttu-id="dd5ee-131">Microsoft. Azure. Commands. ServiceBus. modeller. PSServiceBusMigrationConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="dd5ee-131">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusMigrationConfigurationAttributes</span></span>

## <span data-ttu-id="dd5ee-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dd5ee-132">NOTES</span></span>

## <span data-ttu-id="dd5ee-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dd5ee-133">RELATED LINKS</span></span>
