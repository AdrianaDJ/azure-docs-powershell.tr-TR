---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/complete-azurermservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Complete-AzureRmServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Complete-AzureRmServiceBusMigration.md
ms.openlocfilehash: 0006e4768dc27994d18e93e48696b5ee9a514c45
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763799"
---
# <span data-ttu-id="3ce61-101">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="3ce61-101">Complete-AzureRmServiceBusMigration</span></span>

## <span data-ttu-id="3ce61-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ce61-102">SYNOPSIS</span></span>
<span data-ttu-id="3ce61-103">Cmdlet 'ler standart 'dan Premium ad alanına tam olarak ve standart ad uzayının bağlantı dizelerini</span><span class="sxs-lookup"><span data-stu-id="3ce61-103">Cmdlets set the Migration from Standard to premium namespace as complete and connection strings of standard namespace now point to Premium namespace</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3ce61-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3ce61-104">SYNTAX</span></span>

### <span data-ttu-id="3ce61-105">MigrationConfigurationPropertiesSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3ce61-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Complete-AzureRmServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ce61-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="3ce61-106">NamespaceInputObjectSet</span></span>
```
Complete-AzureRmServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ce61-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ce61-107">NamespaceResourceIdParameterSet</span></span>
```
Complete-AzureRmServiceBusMigration [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ce61-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="3ce61-108">DESCRIPTION</span></span>
<span data-ttu-id="3ce61-109">**Tam-AzureRmServiceBusMigration** cmdlet 'leri standarttan Premium ad alanına tam olarak</span><span class="sxs-lookup"><span data-stu-id="3ce61-109">The **Complete-AzureRmServiceBusMigration** cmdlets set the Migration from Standard to premium namespace as complete and connection strings of standard namespace now point to Premium namespace</span></span>

## <span data-ttu-id="3ce61-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3ce61-110">EXAMPLES</span></span>

### <span data-ttu-id="3ce61-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="3ce61-111">Example 1</span></span>
```powershell
PS C:\> Complete-AzureRmServiceBusMigration -ResourceGroupName ResourceGroup -Name NamespaceStandardMirgation
```

<span data-ttu-id="3ce61-112">' Namespacestandardir, ' ad alanının geçişini tamamlandı olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="3ce61-112">Sets the Migration of 'NamespaceStandardMirgation' namespace as complete.</span></span>

## <span data-ttu-id="3ce61-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3ce61-113">PARAMETERS</span></span>

### <span data-ttu-id="3ce61-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ce61-114">-DefaultProfile</span></span>
<span data-ttu-id="3ce61-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3ce61-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ce61-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3ce61-116">-InputObject</span></span>
<span data-ttu-id="3ce61-117">Hizmet veri yolu geçiş yapılandırması-standart ad alanı nesnesi</span><span class="sxs-lookup"><span data-stu-id="3ce61-117">Service Bus Migration configuration - Standard Namespace Object</span></span>

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

### <span data-ttu-id="3ce61-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="3ce61-118">-Name</span></span>
<span data-ttu-id="3ce61-119">Standart ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="3ce61-119">Standard Namespace Name</span></span>

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

### <span data-ttu-id="3ce61-120">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="3ce61-120">-PassThru</span></span>
<span data-ttu-id="3ce61-121">Komut başarılı olmuşsa, bunu belirtmek doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="3ce61-121">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="3ce61-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ce61-122">-ResourceGroupName</span></span>
<span data-ttu-id="3ce61-123">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="3ce61-123">Resource Group Name</span></span>

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

### <span data-ttu-id="3ce61-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="3ce61-124">-ResourceId</span></span>
<span data-ttu-id="3ce61-125">Hizmet veri yolu Migratio-standart ad alanı kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="3ce61-125">Service Bus Migratio - Standard Namespace Resource Id</span></span>

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

### <span data-ttu-id="3ce61-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="3ce61-126">-Confirm</span></span>
<span data-ttu-id="3ce61-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3ce61-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ce61-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ce61-128">-WhatIf</span></span>
<span data-ttu-id="3ce61-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3ce61-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ce61-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3ce61-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ce61-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ce61-131">CommonParameters</span></span>
<span data-ttu-id="3ce61-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3ce61-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ce61-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ce61-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ce61-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3ce61-134">INPUTS</span></span>

### <span data-ttu-id="3ce61-135">Microsoft. Azure. Commands. ServiceBus. model. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="3ce61-135">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>
<span data-ttu-id="3ce61-136">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3ce61-136">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="3ce61-137">System. String</span><span class="sxs-lookup"><span data-stu-id="3ce61-137">System.String</span></span>

## <span data-ttu-id="3ce61-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3ce61-138">OUTPUTS</span></span>

### <span data-ttu-id="3ce61-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3ce61-139">System.Boolean</span></span>

## <span data-ttu-id="3ce61-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3ce61-140">NOTES</span></span>

## <span data-ttu-id="3ce61-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3ce61-141">RELATED LINKS</span></span>
