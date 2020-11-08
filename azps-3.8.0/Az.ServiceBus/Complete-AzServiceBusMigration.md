---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/complete-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Complete-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Complete-AzServiceBusMigration.md
ms.openlocfilehash: 883ecf9337cea2b46166b4c1be8625c9763eb7db
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94103756"
---
# <span data-ttu-id="1808e-101">Complete-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="1808e-101">Complete-AzServiceBusMigration</span></span>

## <span data-ttu-id="1808e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1808e-102">SYNOPSIS</span></span>
<span data-ttu-id="1808e-103">Cmdlet 'ler standart 'dan Premium ad alanına tam olarak ve standart ad uzayının bağlantı dizelerini</span><span class="sxs-lookup"><span data-stu-id="1808e-103">Cmdlets set the Migration from Standard to premium namespace as complete and connection strings of standard namespace now point to Premium namespace</span></span>

## <span data-ttu-id="1808e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1808e-104">SYNTAX</span></span>

### <span data-ttu-id="1808e-105">MigrationConfigurationPropertiesSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1808e-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Complete-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1808e-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="1808e-106">NamespaceInputObjectSet</span></span>
```
Complete-AzServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1808e-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1808e-107">NamespaceResourceIdParameterSet</span></span>
```
Complete-AzServiceBusMigration [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1808e-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="1808e-108">DESCRIPTION</span></span>
<span data-ttu-id="1808e-109">**Complete-Azhizmetibusmigration** cmdlet 'leri standarttan Premium ad alanına tam olarak</span><span class="sxs-lookup"><span data-stu-id="1808e-109">The **Complete-AzServiceBusMigration** cmdlets set the Migration from Standard to premium namespace as complete and connection strings of standard namespace now point to Premium namespace</span></span>

## <span data-ttu-id="1808e-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1808e-110">EXAMPLES</span></span>

### <span data-ttu-id="1808e-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1808e-111">Example 1</span></span>
```powershell
PS C:\> Complete-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name NamespaceStandardMigration
```

<span data-ttu-id="1808e-112">' NamespaceStandardMigration ' ad alanının geçişini tamamlandı olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="1808e-112">Sets the Migration of 'NamespaceStandardMigration' namespace as complete.</span></span>

## <span data-ttu-id="1808e-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1808e-113">PARAMETERS</span></span>

### <span data-ttu-id="1808e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1808e-114">-DefaultProfile</span></span>
<span data-ttu-id="1808e-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1808e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1808e-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1808e-116">-InputObject</span></span>
<span data-ttu-id="1808e-117">Hizmet veri yolu geçiş yapılandırması-standart ad alanı nesnesi</span><span class="sxs-lookup"><span data-stu-id="1808e-117">Service Bus Migration configuration - Standard Namespace Object</span></span>

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

### <span data-ttu-id="1808e-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="1808e-118">-Name</span></span>
<span data-ttu-id="1808e-119">Standart ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="1808e-119">Standard Namespace Name</span></span>

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

### <span data-ttu-id="1808e-120">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="1808e-120">-PassThru</span></span>
<span data-ttu-id="1808e-121">Komut başarılı olmuşsa, bunu belirtmek doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="1808e-121">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="1808e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1808e-122">-ResourceGroupName</span></span>
<span data-ttu-id="1808e-123">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="1808e-123">Resource Group Name</span></span>

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

### <span data-ttu-id="1808e-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="1808e-124">-ResourceId</span></span>
<span data-ttu-id="1808e-125">Hizmet veri yolu geçişi-standart ad alanı kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="1808e-125">Service Bus Migration - Standard Namespace Resource Id</span></span>

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

### <span data-ttu-id="1808e-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="1808e-126">-Confirm</span></span>
<span data-ttu-id="1808e-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1808e-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1808e-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1808e-128">-WhatIf</span></span>
<span data-ttu-id="1808e-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1808e-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1808e-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1808e-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1808e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1808e-131">CommonParameters</span></span>
<span data-ttu-id="1808e-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1808e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1808e-133">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1808e-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1808e-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1808e-134">INPUTS</span></span>

### <span data-ttu-id="1808e-135">Microsoft. Azure. Commands. ServiceBus. model. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="1808e-135">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

### <span data-ttu-id="1808e-136">System. String</span><span class="sxs-lookup"><span data-stu-id="1808e-136">System.String</span></span>

## <span data-ttu-id="1808e-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1808e-137">OUTPUTS</span></span>

### <span data-ttu-id="1808e-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1808e-138">System.Boolean</span></span>

## <span data-ttu-id="1808e-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1808e-139">NOTES</span></span>

## <span data-ttu-id="1808e-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1808e-140">RELATED LINKS</span></span>
