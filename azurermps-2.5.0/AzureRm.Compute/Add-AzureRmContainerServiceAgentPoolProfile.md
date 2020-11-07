---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: C3C65F3E-1192-4B57-87DB-5D371C8FF68E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermcontainerserviceagentpoolprofile
schema: 2.0.0
ms.openlocfilehash: a89494b155755cf716f39275debcfb7477071da2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939617"
---
# <span data-ttu-id="a79d6-101">Add-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="a79d6-101">Add-AzureRmContainerServiceAgentPoolProfile</span></span>

## <span data-ttu-id="a79d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a79d6-102">SYNOPSIS</span></span>
<span data-ttu-id="a79d6-103">Kapsayıcı hizmet Aracısı havuz profili ekler.</span><span class="sxs-lookup"><span data-stu-id="a79d6-103">Adds a container service agent pool profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a79d6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a79d6-104">SYNTAX</span></span>

```
Add-AzureRmContainerServiceAgentPoolProfile [-ContainerService] <PSContainerService> [[-Name] <String>]
 [[-Count] <Int32>] [[-VmSize] <String>] [[-DnsPrefix] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a79d6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a79d6-105">DESCRIPTION</span></span>
<span data-ttu-id="a79d6-106">**Add-AzureRmContainerServiceAgentPoolProfile** cmdlet 'i yerel kapsayıcı hizmet nesnesine kapsayıcı hizmet Aracısı havuzu profili ekler.</span><span class="sxs-lookup"><span data-stu-id="a79d6-106">The **Add-AzureRmContainerServiceAgentPoolProfile** cmdlet adds a container service agent pool profile to a local container service object.</span></span>

## <span data-ttu-id="a79d6-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a79d6-107">EXAMPLES</span></span>

### <span data-ttu-id="a79d6-108">Örnek 1: profil ekleme</span><span class="sxs-lookup"><span data-stu-id="a79d6-108">Example 1: Add a profile</span></span>
```
PS C:\> Add-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
```

<span data-ttu-id="a79d6-109">Bu komut, yerel kapsayıcı hizmet nesnesine kapsayıcı hizmet Aracısı havuzu profili ekler.</span><span class="sxs-lookup"><span data-stu-id="a79d6-109">This command adds a container service agent pool profile to the local container service object.</span></span>

## <span data-ttu-id="a79d6-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a79d6-110">PARAMETERS</span></span>

### <span data-ttu-id="a79d6-111">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="a79d6-111">-ContainerService</span></span>
<span data-ttu-id="a79d6-112">Bu cmdlet 'in bir aracı havuz profili eklediği kapsayıcı hizmeti nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a79d6-112">Specifies the container service object to which this cmdlet adds an agent pool profile.</span></span>
<span data-ttu-id="a79d6-113">**Containerservice** nesnesi edinmek Için, [New-AzureRmContainerServiceConfig](./New-AzureRmContainerServiceConfig.md) cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="a79d6-113">To obtain a **ContainerService** object, use the [New-AzureRmContainerServiceConfig](./New-AzureRmContainerServiceConfig.md) cmdlet.</span></span>

```yaml
Type: PSContainerService
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a79d6-114">-Sayı</span><span class="sxs-lookup"><span data-stu-id="a79d6-114">-Count</span></span>
<span data-ttu-id="a79d6-115">Kapsayıcıları barındıran aracıların sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a79d6-115">Specifies the number of agents that host containers.</span></span>
<span data-ttu-id="a79d6-116">Bu parametre için kabul edilebilir değerler: 1 ile 100 arasındaki tamsayılardır.</span><span class="sxs-lookup"><span data-stu-id="a79d6-116">The acceptable values for this parameter are: integers from 1 to 100.</span></span>
<span data-ttu-id="a79d6-117">Varsayılan değer 1 ' dir.</span><span class="sxs-lookup"><span data-stu-id="a79d6-117">The default value is 1.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a79d6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a79d6-118">-DefaultProfile</span></span>
<span data-ttu-id="a79d6-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a79d6-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a79d6-120">-DnsPrefix</span><span class="sxs-lookup"><span data-stu-id="a79d6-120">-DnsPrefix</span></span>
<span data-ttu-id="a79d6-121">Bu aracı havuzunun tam nitelikli etki alanı adını oluşturmak için bu cmdlet 'in kullandığı DNS önekini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a79d6-121">Specifies the DNS prefix that this cmdlet uses to create the fully qualified domain name for this agent pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a79d6-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="a79d6-122">-Name</span></span>
<span data-ttu-id="a79d6-123">Aracı havuz profilinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a79d6-123">Specifies the name of the agent pool profile.</span></span>
<span data-ttu-id="a79d6-124">Bu değer, abonelik ve kaynak grubu bağlamında benzersiz olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="a79d6-124">This value must be unique in the context of the subscription and resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a79d6-125">-VmSize</span><span class="sxs-lookup"><span data-stu-id="a79d6-125">-VmSize</span></span>
<span data-ttu-id="a79d6-126">Aracıların sanal makinelerin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="a79d6-126">Specifies the size of the virtual machines for the agents.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a79d6-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="a79d6-127">-Confirm</span></span>
<span data-ttu-id="a79d6-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a79d6-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a79d6-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a79d6-129">-WhatIf</span></span>
<span data-ttu-id="a79d6-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a79d6-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a79d6-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a79d6-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a79d6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a79d6-132">CommonParameters</span></span>
<span data-ttu-id="a79d6-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a79d6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a79d6-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a79d6-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a79d6-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a79d6-135">INPUTS</span></span>

### <span data-ttu-id="a79d6-136">ContainerService</span><span class="sxs-lookup"><span data-stu-id="a79d6-136">ContainerService</span></span>
<span data-ttu-id="a79d6-137">Parametre ' ContainerService ', ardışık düzenin ' ContainerService ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="a79d6-137">Parameter 'ContainerService' accepts value of type 'ContainerService' from the pipeline</span></span>

## <span data-ttu-id="a79d6-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a79d6-138">OUTPUTS</span></span>

### <span data-ttu-id="a79d6-139">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="a79d6-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="a79d6-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a79d6-140">NOTES</span></span>

## <span data-ttu-id="a79d6-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a79d6-141">RELATED LINKS</span></span>

[<span data-ttu-id="a79d6-142">Yeni-AzureRmContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="a79d6-142">New-AzureRmContainerServiceConfig</span></span>](./New-AzureRmContainerServiceConfig.md)

[<span data-ttu-id="a79d6-143">Remove-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="a79d6-143">Remove-AzureRmContainerServiceAgentPoolProfile</span></span>](./Remove-AzureRmContainerServiceAgentPoolProfile.md)
