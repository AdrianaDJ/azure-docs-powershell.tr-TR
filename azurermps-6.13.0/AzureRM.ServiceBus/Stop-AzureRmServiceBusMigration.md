---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/stop-azurermservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Stop-AzureRmServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Stop-AzureRmServiceBusMigration.md
ms.openlocfilehash: 25a8b6918c5cd10a2f47230274c357008731ffba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590852"
---
# <span data-ttu-id="82a4a-101">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="82a4a-101">Stop-AzureRmServiceBusMigration</span></span>

## <span data-ttu-id="82a4a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82a4a-102">SYNOPSIS</span></span>
<span data-ttu-id="82a4a-103">{{Synopsis} doldurun}}</span><span class="sxs-lookup"><span data-stu-id="82a4a-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="82a4a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="82a4a-104">SYNTAX</span></span>

### <span data-ttu-id="82a4a-105">MigrationConfigurationPropertiesSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="82a4a-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Stop-AzureRmServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82a4a-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="82a4a-106">NamespaceInputObjectSet</span></span>
```
Stop-AzureRmServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82a4a-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="82a4a-107">NamespaceResourceIdParameterSet</span></span>
```
Stop-AzureRmServiceBusMigration [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82a4a-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="82a4a-108">DESCRIPTION</span></span>
<span data-ttu-id="82a4a-109">**Stop-AzureRmServiceBusMigration** cmdlet 'leri</span><span class="sxs-lookup"><span data-stu-id="82a4a-109">The **Stop-AzureRmServiceBusMigration** cmdlets  tremitates the Migration between Standard to premium namespace</span></span>

## <span data-ttu-id="82a4a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="82a4a-110">EXAMPLES</span></span>

### <span data-ttu-id="82a4a-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="82a4a-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzureRmServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMirgation
```

<span data-ttu-id="82a4a-112">cmdlet, geçiş yapılandırmasını oluştururken sağlanan standart ad alanı ile Premium ad alanı arasındaki geçişe sahiptir.</span><span class="sxs-lookup"><span data-stu-id="82a4a-112">cmdlet termitates the migration between Standard namespace and Premium namespace provided while creating the migration configuration.</span></span>

## <span data-ttu-id="82a4a-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="82a4a-113">PARAMETERS</span></span>

### <span data-ttu-id="82a4a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82a4a-114">-DefaultProfile</span></span>
<span data-ttu-id="82a4a-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="82a4a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82a4a-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="82a4a-116">-InputObject</span></span>
<span data-ttu-id="82a4a-117">Hizmet veri yolu geçiş yapılandırması standart ad alanı nesnesi</span><span class="sxs-lookup"><span data-stu-id="82a4a-117">Service Bus Migration Configuration Standard Namespace Object</span></span>

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

### <span data-ttu-id="82a4a-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="82a4a-118">-Name</span></span>
<span data-ttu-id="82a4a-119">Standart ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="82a4a-119">Standard Namespace Name</span></span>

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

### <span data-ttu-id="82a4a-120">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="82a4a-120">-PassThru</span></span>
<span data-ttu-id="82a4a-121">Komut başarılı olmuşsa, bunu belirtmek doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="82a4a-121">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="82a4a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82a4a-122">-ResourceGroupName</span></span>
<span data-ttu-id="82a4a-123">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="82a4a-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: MigrationConfigurationPropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82a4a-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="82a4a-124">-ResourceId</span></span>
<span data-ttu-id="82a4a-125">Hizmet veri yolu geçiş yapılandırması standart ad alanı kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="82a4a-125">Service Bus Migration Configuration Standard Namespace Resource Id</span></span>

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

### <span data-ttu-id="82a4a-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="82a4a-126">-Confirm</span></span>
<span data-ttu-id="82a4a-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="82a4a-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82a4a-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82a4a-128">-WhatIf</span></span>
<span data-ttu-id="82a4a-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="82a4a-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82a4a-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="82a4a-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82a4a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82a4a-131">CommonParameters</span></span>
<span data-ttu-id="82a4a-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="82a4a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82a4a-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82a4a-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82a4a-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="82a4a-134">INPUTS</span></span>

### <span data-ttu-id="82a4a-135">Microsoft. Azure. Commands. ServiceBus. model. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="82a4a-135">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>
<span data-ttu-id="82a4a-136">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="82a4a-136">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="82a4a-137">System. String</span><span class="sxs-lookup"><span data-stu-id="82a4a-137">System.String</span></span>

## <span data-ttu-id="82a4a-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="82a4a-138">OUTPUTS</span></span>

### <span data-ttu-id="82a4a-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="82a4a-139">System.Boolean</span></span>

## <span data-ttu-id="82a4a-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="82a4a-140">NOTES</span></span>

## <span data-ttu-id="82a4a-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="82a4a-141">RELATED LINKS</span></span>
