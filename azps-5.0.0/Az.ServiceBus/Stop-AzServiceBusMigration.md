---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/stop-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Stop-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Stop-AzServiceBusMigration.md
ms.openlocfilehash: 615a09d735867d45f9db75ce229d39bc8d9bf75b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276178"
---
# <span data-ttu-id="36ef1-101">Stop-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="36ef1-101">Stop-AzServiceBusMigration</span></span>

## <span data-ttu-id="36ef1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36ef1-102">SYNOPSIS</span></span>
<span data-ttu-id="36ef1-103">{{Synopsis} doldurun}}</span><span class="sxs-lookup"><span data-stu-id="36ef1-103">{{Fill in the Synopsis}}</span></span>

## <span data-ttu-id="36ef1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="36ef1-104">SYNTAX</span></span>

### <span data-ttu-id="36ef1-105">MigrationConfigurationPropertiesSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="36ef1-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Stop-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36ef1-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="36ef1-106">NamespaceInputObjectSet</span></span>
```
Stop-AzServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36ef1-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="36ef1-107">NamespaceResourceIdParameterSet</span></span>
```
Stop-AzServiceBusMigration [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36ef1-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="36ef1-108">DESCRIPTION</span></span>
<span data-ttu-id="36ef1-109">**Stop-AzServiceBusMigration** cmdlet 'leri standart ile Premium ad alanı arasındaki geçişi sonlandırır</span><span class="sxs-lookup"><span data-stu-id="36ef1-109">The **Stop-AzServiceBusMigration** cmdlets terminates the Migration between Standard to premium namespace</span></span>

## <span data-ttu-id="36ef1-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="36ef1-110">EXAMPLES</span></span>

### <span data-ttu-id="36ef1-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="36ef1-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMigration
```

<span data-ttu-id="36ef1-112">Cmdlet, geçiş yapılandırmasını oluştururken sağlanan standart ad alanı ile Premium ad alanı arasındaki geçişi sonlandırır.</span><span class="sxs-lookup"><span data-stu-id="36ef1-112">Cmdlet terminates the migration between Standard namespace and Premium namespace provided while creating the migration configuration.</span></span>

## <span data-ttu-id="36ef1-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="36ef1-113">PARAMETERS</span></span>

### <span data-ttu-id="36ef1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36ef1-114">-DefaultProfile</span></span>
<span data-ttu-id="36ef1-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="36ef1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36ef1-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="36ef1-116">-InputObject</span></span>
<span data-ttu-id="36ef1-117">Hizmet veri yolu geçiş yapılandırması standart ad alanı nesnesi</span><span class="sxs-lookup"><span data-stu-id="36ef1-117">Service Bus Migration Configuration Standard Namespace Object</span></span>

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

### <span data-ttu-id="36ef1-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="36ef1-118">-Name</span></span>
<span data-ttu-id="36ef1-119">Standart ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="36ef1-119">Standard Namespace Name</span></span>

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

### <span data-ttu-id="36ef1-120">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="36ef1-120">-PassThru</span></span>
<span data-ttu-id="36ef1-121">Komut başarılı olmuşsa, bunu belirtmek doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="36ef1-121">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="36ef1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36ef1-122">-ResourceGroupName</span></span>
<span data-ttu-id="36ef1-123">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="36ef1-123">Resource Group Name</span></span>

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

### <span data-ttu-id="36ef1-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="36ef1-124">-ResourceId</span></span>
<span data-ttu-id="36ef1-125">Hizmet veri yolu geçiş yapılandırması standart ad alanı kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="36ef1-125">Service Bus Migration Configuration Standard Namespace Resource Id</span></span>

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

### <span data-ttu-id="36ef1-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="36ef1-126">-Confirm</span></span>
<span data-ttu-id="36ef1-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="36ef1-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36ef1-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36ef1-128">-WhatIf</span></span>
<span data-ttu-id="36ef1-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="36ef1-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36ef1-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="36ef1-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36ef1-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36ef1-131">CommonParameters</span></span>
<span data-ttu-id="36ef1-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="36ef1-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36ef1-133">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36ef1-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36ef1-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="36ef1-134">INPUTS</span></span>

### <span data-ttu-id="36ef1-135">Microsoft. Azure. Commands. ServiceBus. model. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="36ef1-135">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

### <span data-ttu-id="36ef1-136">System. String</span><span class="sxs-lookup"><span data-stu-id="36ef1-136">System.String</span></span>

## <span data-ttu-id="36ef1-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="36ef1-137">OUTPUTS</span></span>

### <span data-ttu-id="36ef1-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="36ef1-138">System.Boolean</span></span>

## <span data-ttu-id="36ef1-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="36ef1-139">NOTES</span></span>

## <span data-ttu-id="36ef1-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="36ef1-140">RELATED LINKS</span></span>
