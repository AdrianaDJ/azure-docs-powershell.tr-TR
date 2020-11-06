---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: C3C65F3E-1192-4B57-87DB-5D371C8FF68E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmContainerServiceAgentPoolProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmContainerServiceAgentPoolProfile.md
ms.openlocfilehash: 1b3df5b930cd7b30af8fef35735eea56eab7a5da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591724"
---
# <span data-ttu-id="286cd-101">Add-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="286cd-101">Add-AzureRmContainerServiceAgentPoolProfile</span></span>

## <span data-ttu-id="286cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="286cd-102">SYNOPSIS</span></span>
<span data-ttu-id="286cd-103">Kapsayıcı hizmet Aracısı havuz profili ekler.</span><span class="sxs-lookup"><span data-stu-id="286cd-103">Adds a container service agent pool profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="286cd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="286cd-104">SYNTAX</span></span>

```
Add-AzureRmContainerServiceAgentPoolProfile [-ContainerService] <ContainerService> [[-Name] <String>]
 [[-Count] <Int32>] [[-VmSize] <String>] [[-DnsPrefix] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="286cd-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="286cd-105">DESCRIPTION</span></span>
<span data-ttu-id="286cd-106">**Add-AzureRmContainerServiceAgentPoolProfile** cmdlet 'i yerel kapsayıcı hizmet nesnesine kapsayıcı hizmet Aracısı havuzu profili ekler.</span><span class="sxs-lookup"><span data-stu-id="286cd-106">The **Add-AzureRmContainerServiceAgentPoolProfile** cmdlet adds a container service agent pool profile to a local container service object.</span></span>

## <span data-ttu-id="286cd-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="286cd-107">EXAMPLES</span></span>

### <span data-ttu-id="286cd-108">Örnek 1: profil ekleme</span><span class="sxs-lookup"><span data-stu-id="286cd-108">Example 1: Add a profile</span></span>
```
PS C:\> Add-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
```

<span data-ttu-id="286cd-109">Bu komut, yerel kapsayıcı hizmet nesnesine kapsayıcı hizmet Aracısı havuzu profili ekler.</span><span class="sxs-lookup"><span data-stu-id="286cd-109">This command adds a container service agent pool profile to the local container service object.</span></span>

## <span data-ttu-id="286cd-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="286cd-110">PARAMETERS</span></span>

### <span data-ttu-id="286cd-111">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="286cd-111">-ContainerService</span></span>
<span data-ttu-id="286cd-112">Bu cmdlet 'in bir aracı havuz profili eklediği kapsayıcı hizmeti nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="286cd-112">Specifies the container service object to which this cmdlet adds an agent pool profile.</span></span>
<span data-ttu-id="286cd-113">**Containerservice** nesnesi edinmek Için, [New-AzureRmContainerServiceConfig](./New-AzureRmContainerServiceConfig.md) cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="286cd-113">To obtain a **ContainerService** object, use the [New-AzureRmContainerServiceConfig](./New-AzureRmContainerServiceConfig.md) cmdlet.</span></span>

```yaml
Type: ContainerService
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="286cd-114">-Sayı</span><span class="sxs-lookup"><span data-stu-id="286cd-114">-Count</span></span>
<span data-ttu-id="286cd-115">Kapsayıcıları barındıran aracıların sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="286cd-115">Specifies the number of agents that host containers.</span></span>
<span data-ttu-id="286cd-116">Bu parametre için kabul edilebilir değerler: 1 ile 100 arasındaki tamsayılardır.</span><span class="sxs-lookup"><span data-stu-id="286cd-116">The acceptable values for this parameter are: integers from 1 to 100.</span></span>
<span data-ttu-id="286cd-117">Varsayılan değer 1 ' dir.</span><span class="sxs-lookup"><span data-stu-id="286cd-117">The default value is 1.</span></span>

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

### <span data-ttu-id="286cd-118">-DnsPrefix</span><span class="sxs-lookup"><span data-stu-id="286cd-118">-DnsPrefix</span></span>
<span data-ttu-id="286cd-119">Bu aracı havuzunun tam nitelikli etki alanı adını oluşturmak için bu cmdlet 'in kullandığı DNS önekini belirtir.</span><span class="sxs-lookup"><span data-stu-id="286cd-119">Specifies the DNS prefix that this cmdlet uses to create the fully qualified domain name for this agent pool.</span></span>

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

### <span data-ttu-id="286cd-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="286cd-120">-Name</span></span>
<span data-ttu-id="286cd-121">Aracı havuz profilinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="286cd-121">Specifies the name of the agent pool profile.</span></span>
<span data-ttu-id="286cd-122">Bu değer, abonelik ve kaynak grubu bağlamında benzersiz olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="286cd-122">This value must be unique in the context of the subscription and resource group.</span></span>

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

### <span data-ttu-id="286cd-123">-VmSize</span><span class="sxs-lookup"><span data-stu-id="286cd-123">-VmSize</span></span>
<span data-ttu-id="286cd-124">Aracıların sanal makinelerin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="286cd-124">Specifies the size of the virtual machines for the agents.</span></span>

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

### <span data-ttu-id="286cd-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="286cd-125">-Confirm</span></span>
<span data-ttu-id="286cd-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="286cd-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="286cd-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="286cd-127">-WhatIf</span></span>
<span data-ttu-id="286cd-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="286cd-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="286cd-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="286cd-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="286cd-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="286cd-130">CommonParameters</span></span>
<span data-ttu-id="286cd-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="286cd-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="286cd-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="286cd-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="286cd-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="286cd-133">INPUTS</span></span>

### <span data-ttu-id="286cd-134">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="286cd-134">None</span></span>
<span data-ttu-id="286cd-135">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="286cd-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="286cd-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="286cd-136">OUTPUTS</span></span>

## <span data-ttu-id="286cd-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="286cd-137">NOTES</span></span>

## <span data-ttu-id="286cd-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="286cd-138">RELATED LINKS</span></span>

[<span data-ttu-id="286cd-139">Yeni-AzureRmContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="286cd-139">New-AzureRmContainerServiceConfig</span></span>](./New-AzureRmContainerServiceConfig.md)

[<span data-ttu-id="286cd-140">Remove-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="286cd-140">Remove-AzureRmContainerServiceAgentPoolProfile</span></span>](./Remove-AzureRmContainerServiceAgentPoolProfile.md)
