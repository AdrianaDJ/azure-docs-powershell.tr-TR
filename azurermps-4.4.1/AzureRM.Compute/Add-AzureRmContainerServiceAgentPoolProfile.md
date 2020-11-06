---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: C3C65F3E-1192-4B57-87DB-5D371C8FF68E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmContainerServiceAgentPoolProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmContainerServiceAgentPoolProfile.md
ms.openlocfilehash: a5ce087e8ebf768b63d09a4002c3aaf38ddd9f84
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594806"
---
# <span data-ttu-id="cb146-101">Add-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="cb146-101">Add-AzureRmContainerServiceAgentPoolProfile</span></span>

## <span data-ttu-id="cb146-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb146-102">SYNOPSIS</span></span>
<span data-ttu-id="cb146-103">Kapsayıcı hizmet Aracısı havuz profili ekler.</span><span class="sxs-lookup"><span data-stu-id="cb146-103">Adds a container service agent pool profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cb146-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cb146-104">SYNTAX</span></span>

```
Add-AzureRmContainerServiceAgentPoolProfile [-ContainerService] <PSContainerService> [[-Name] <String>]
 [[-Count] <Int32>] [[-VmSize] <String>] [[-DnsPrefix] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb146-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="cb146-105">DESCRIPTION</span></span>
<span data-ttu-id="cb146-106">**Add-AzureRmContainerServiceAgentPoolProfile** cmdlet 'i yerel kapsayıcı hizmet nesnesine kapsayıcı hizmet Aracısı havuzu profili ekler.</span><span class="sxs-lookup"><span data-stu-id="cb146-106">The **Add-AzureRmContainerServiceAgentPoolProfile** cmdlet adds a container service agent pool profile to a local container service object.</span></span>

## <span data-ttu-id="cb146-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cb146-107">EXAMPLES</span></span>

### <span data-ttu-id="cb146-108">Örnek 1: profil ekleme</span><span class="sxs-lookup"><span data-stu-id="cb146-108">Example 1: Add a profile</span></span>
```
PS C:\> Add-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
```

<span data-ttu-id="cb146-109">Bu komut, yerel kapsayıcı hizmet nesnesine kapsayıcı hizmet Aracısı havuzu profili ekler.</span><span class="sxs-lookup"><span data-stu-id="cb146-109">This command adds a container service agent pool profile to the local container service object.</span></span>

## <span data-ttu-id="cb146-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cb146-110">PARAMETERS</span></span>

### <span data-ttu-id="cb146-111">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="cb146-111">-ContainerService</span></span>
<span data-ttu-id="cb146-112">Bu cmdlet 'in bir aracı havuz profili eklediği kapsayıcı hizmeti nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="cb146-112">Specifies the container service object to which this cmdlet adds an agent pool profile.</span></span>
<span data-ttu-id="cb146-113">**Containerservice** nesnesi edinmek Için, [New-AzureRmContainerServiceConfig](./New-AzureRmContainerServiceConfig.md) cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="cb146-113">To obtain a **ContainerService** object, use the [New-AzureRmContainerServiceConfig](./New-AzureRmContainerServiceConfig.md) cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cb146-114">-Sayı</span><span class="sxs-lookup"><span data-stu-id="cb146-114">-Count</span></span>
<span data-ttu-id="cb146-115">Kapsayıcıları barındıran aracıların sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cb146-115">Specifies the number of agents that host containers.</span></span>
<span data-ttu-id="cb146-116">Bu parametre için kabul edilebilir değerler: 1 ile 100 arasındaki tamsayılardır.</span><span class="sxs-lookup"><span data-stu-id="cb146-116">The acceptable values for this parameter are: integers from 1 to 100.</span></span>
<span data-ttu-id="cb146-117">Varsayılan değer 1 ' dir.</span><span class="sxs-lookup"><span data-stu-id="cb146-117">The default value is 1.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb146-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb146-118">-DefaultProfile</span></span>
<span data-ttu-id="cb146-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cb146-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb146-120">-DnsPrefix</span><span class="sxs-lookup"><span data-stu-id="cb146-120">-DnsPrefix</span></span>
<span data-ttu-id="cb146-121">Bu aracı havuzunun tam nitelikli etki alanı adını oluşturmak için bu cmdlet 'in kullandığı DNS önekini belirtir.</span><span class="sxs-lookup"><span data-stu-id="cb146-121">Specifies the DNS prefix that this cmdlet uses to create the fully qualified domain name for this agent pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb146-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="cb146-122">-Name</span></span>
<span data-ttu-id="cb146-123">Aracı havuz profilinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cb146-123">Specifies the name of the agent pool profile.</span></span>
<span data-ttu-id="cb146-124">Bu değer, abonelik ve kaynak grubu bağlamında benzersiz olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="cb146-124">This value must be unique in the context of the subscription and resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb146-125">-VmSize</span><span class="sxs-lookup"><span data-stu-id="cb146-125">-VmSize</span></span>
<span data-ttu-id="cb146-126">Aracıların sanal makinelerin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="cb146-126">Specifies the size of the virtual machines for the agents.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb146-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="cb146-127">-Confirm</span></span>
<span data-ttu-id="cb146-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="cb146-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb146-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb146-129">-WhatIf</span></span>
<span data-ttu-id="cb146-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="cb146-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cb146-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="cb146-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb146-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb146-132">CommonParameters</span></span>
<span data-ttu-id="cb146-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cb146-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb146-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb146-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb146-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cb146-135">INPUTS</span></span>

## <span data-ttu-id="cb146-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cb146-136">OUTPUTS</span></span>

## <span data-ttu-id="cb146-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cb146-137">NOTES</span></span>

## <span data-ttu-id="cb146-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cb146-138">RELATED LINKS</span></span>

[<span data-ttu-id="cb146-139">Yeni-AzureRmContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="cb146-139">New-AzureRmContainerServiceConfig</span></span>](./New-AzureRmContainerServiceConfig.md)

[<span data-ttu-id="cb146-140">Remove-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="cb146-140">Remove-AzureRmContainerServiceAgentPoolProfile</span></span>](./Remove-AzureRmContainerServiceAgentPoolProfile.md)
