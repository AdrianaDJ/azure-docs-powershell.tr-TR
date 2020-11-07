---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/stop-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Stop-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Stop-AzServiceBusMigration.md
ms.openlocfilehash: c507caa0ce6697132876309a7ae816802a682683
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759132"
---
# <span data-ttu-id="f0aa0-101">Stop-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="f0aa0-101">Stop-AzServiceBusMigration</span></span>

## <span data-ttu-id="f0aa0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0aa0-102">SYNOPSIS</span></span>
<span data-ttu-id="f0aa0-103">{{Synopsis} doldurun}}</span><span class="sxs-lookup"><span data-stu-id="f0aa0-103">{{Fill in the Synopsis}}</span></span>

## <span data-ttu-id="f0aa0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f0aa0-104">SYNTAX</span></span>

### <span data-ttu-id="f0aa0-105">MigrationConfigurationPropertiesSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f0aa0-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Stop-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0aa0-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f0aa0-106">NamespaceInputObjectSet</span></span>
```
Stop-AzServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0aa0-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f0aa0-107">NamespaceResourceIdParameterSet</span></span>
```
Stop-AzServiceBusMigration [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0aa0-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="f0aa0-108">DESCRIPTION</span></span>
<span data-ttu-id="f0aa0-109">**Stop-AzServiceBusMigration** cmdlet 'leri standart ile Premium ad alanı arasındaki geçişi sonlandırır</span><span class="sxs-lookup"><span data-stu-id="f0aa0-109">The **Stop-AzServiceBusMigration** cmdlets terminates the Migration between Standard to premium namespace</span></span>

## <span data-ttu-id="f0aa0-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f0aa0-110">EXAMPLES</span></span>

### <span data-ttu-id="f0aa0-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f0aa0-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMirgation
```

<span data-ttu-id="f0aa0-112">Cmdlet, geçiş yapılandırmasını oluştururken sağlanan standart ad alanı ile Premium ad alanı arasındaki geçişi sonlandırır.</span><span class="sxs-lookup"><span data-stu-id="f0aa0-112">Cmdlet terminates the migration between Standard namespace and Premium namespace provided while creating the migration configuration.</span></span>

## <span data-ttu-id="f0aa0-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f0aa0-113">PARAMETERS</span></span>

### <span data-ttu-id="f0aa0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0aa0-114">-DefaultProfile</span></span>
<span data-ttu-id="f0aa0-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f0aa0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0aa0-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f0aa0-116">-InputObject</span></span>
<span data-ttu-id="f0aa0-117">Hizmet veri yolu geçiş yapılandırması standart ad alanı nesnesi</span><span class="sxs-lookup"><span data-stu-id="f0aa0-117">Service Bus Migration Configuration Standard Namespace Object</span></span>

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

### <span data-ttu-id="f0aa0-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="f0aa0-118">-Name</span></span>
<span data-ttu-id="f0aa0-119">Standart ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="f0aa0-119">Standard Namespace Name</span></span>

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

### <span data-ttu-id="f0aa0-120">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="f0aa0-120">-PassThru</span></span>
<span data-ttu-id="f0aa0-121">Komut başarılı olmuşsa, bunu belirtmek doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="f0aa0-121">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="f0aa0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0aa0-122">-ResourceGroupName</span></span>
<span data-ttu-id="f0aa0-123">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="f0aa0-123">Resource Group Name</span></span>

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

### <span data-ttu-id="f0aa0-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="f0aa0-124">-ResourceId</span></span>
<span data-ttu-id="f0aa0-125">Hizmet veri yolu geçiş yapılandırması standart ad alanı kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="f0aa0-125">Service Bus Migration Configuration Standard Namespace Resource Id</span></span>

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

### <span data-ttu-id="f0aa0-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="f0aa0-126">-Confirm</span></span>
<span data-ttu-id="f0aa0-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f0aa0-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0aa0-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0aa0-128">-WhatIf</span></span>
<span data-ttu-id="f0aa0-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f0aa0-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0aa0-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f0aa0-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0aa0-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0aa0-131">CommonParameters</span></span>
<span data-ttu-id="f0aa0-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f0aa0-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0aa0-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0aa0-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0aa0-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f0aa0-134">INPUTS</span></span>

### <span data-ttu-id="f0aa0-135">Microsoft. Azure. Commands. ServiceBus. model. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="f0aa0-135">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

### <span data-ttu-id="f0aa0-136">System. String</span><span class="sxs-lookup"><span data-stu-id="f0aa0-136">System.String</span></span>

## <span data-ttu-id="f0aa0-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f0aa0-137">OUTPUTS</span></span>

### <span data-ttu-id="f0aa0-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f0aa0-138">System.Boolean</span></span>

## <span data-ttu-id="f0aa0-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f0aa0-139">NOTES</span></span>

## <span data-ttu-id="f0aa0-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f0aa0-140">RELATED LINKS</span></span>
