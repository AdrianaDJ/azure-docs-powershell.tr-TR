---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricNodeType.md
ms.openlocfilehash: 305e406a3f2ef723eb0431b495106bb688ffe61c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592547"
---
# <span data-ttu-id="2c8a2-101">Add-AzureRmServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="2c8a2-101">Add-AzureRmServiceFabricNodeType</span></span>

## <span data-ttu-id="2c8a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c8a2-102">SYNOPSIS</span></span>
<span data-ttu-id="2c8a2-103">Var olan kümeye yeni bir düğüm türü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="2c8a2-103">Add a new node type to the existing cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2c8a2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2c8a2-104">SYNTAX</span></span>

```
Add-AzureRmServiceFabricNodeType [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 -Capacity <Int32> -VmUserName <String> -VmPassword <SecureString> [-VmSku <String>] [-Tier <String>]
 [-DurabilityLevel <DurabilityLevel>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2c8a2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2c8a2-105">DESCRIPTION</span></span>
<span data-ttu-id="2c8a2-106">Var olan bir kümeye yeni düğüm türü ekleme.</span><span class="sxs-lookup"><span data-stu-id="2c8a2-106">Add a new node type to a existing cluster.</span></span>

## <span data-ttu-id="2c8a2-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2c8a2-107">EXAMPLES</span></span>

### <span data-ttu-id="2c8a2-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2c8a2-108">Example 1</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String 'Password$123456' -AsPlainText -Force
PS C:\> Add-AzureRmServiceFabricNodeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeType 'n2' -Capacity 5 -VmUserName 'adminName' -VmPassword $pwd
```

<span data-ttu-id="2c8a2-109">Bu komut, kapasitesi 5 olan ve VM Yöneticisi adı ' adminName ' olan yeni bir NodeType ' N2 '.</span><span class="sxs-lookup"><span data-stu-id="2c8a2-109">This command will add a new NodeType 'n2' with capacity of 5, and the vm admin name is 'adminName'.</span></span>

## <span data-ttu-id="2c8a2-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2c8a2-110">PARAMETERS</span></span>

### <span data-ttu-id="2c8a2-111">-Kapasite</span><span class="sxs-lookup"><span data-stu-id="2c8a2-111">-Capacity</span></span>
<span data-ttu-id="2c8a2-112">Kapasitede</span><span class="sxs-lookup"><span data-stu-id="2c8a2-112">Capacity</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2c8a2-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="2c8a2-113">-Name</span></span>
<span data-ttu-id="2c8a2-114">Kümenin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="2c8a2-114">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c8a2-115">-NodeType</span><span class="sxs-lookup"><span data-stu-id="2c8a2-115">-NodeType</span></span>
<span data-ttu-id="2c8a2-116">Düğüm türü adı.</span><span class="sxs-lookup"><span data-stu-id="2c8a2-116">The node type name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2c8a2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c8a2-117">-ResourceGroupName</span></span>
<span data-ttu-id="2c8a2-118">Kaynak grubunun adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="2c8a2-118">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c8a2-119">Katmanlı</span><span class="sxs-lookup"><span data-stu-id="2c8a2-119">-Tier</span></span>
<span data-ttu-id="2c8a2-120">VM SKU katmanı.</span><span class="sxs-lookup"><span data-stu-id="2c8a2-120">Vm Sku Tier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2c8a2-121">-Dur, Itylevel</span><span class="sxs-lookup"><span data-stu-id="2c8a2-121">-DurabilityLevel</span></span>
<span data-ttu-id="2c8a2-122">NodeType 'in dayanıklılık düzeyini belirtin.</span><span class="sxs-lookup"><span data-stu-id="2c8a2-122">Specify the durability level of the NodeType.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel
Parameter Sets: (All)
Aliases: 
Accepted values: Bronze, Silver, Gold

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2c8a2-123">-VmPassword</span><span class="sxs-lookup"><span data-stu-id="2c8a2-123">-VmPassword</span></span>
<span data-ttu-id="2c8a2-124">VM 'de oturum açma parolası.</span><span class="sxs-lookup"><span data-stu-id="2c8a2-124">The password of login to the Vm.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2c8a2-125">-VmSku</span><span class="sxs-lookup"><span data-stu-id="2c8a2-125">-VmSku</span></span>
<span data-ttu-id="2c8a2-126">SKU adı.</span><span class="sxs-lookup"><span data-stu-id="2c8a2-126">The sku name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2c8a2-127">-VmUserName</span><span class="sxs-lookup"><span data-stu-id="2c8a2-127">-VmUserName</span></span>
<span data-ttu-id="2c8a2-128">VM için oturum açma Kullanıcı adı.</span><span class="sxs-lookup"><span data-stu-id="2c8a2-128">The user name for login to Vm.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2c8a2-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="2c8a2-129">-Confirm</span></span>
<span data-ttu-id="2c8a2-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2c8a2-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c8a2-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c8a2-131">-WhatIf</span></span>
<span data-ttu-id="2c8a2-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2c8a2-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2c8a2-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2c8a2-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c8a2-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c8a2-134">-DefaultProfile</span></span>
<span data-ttu-id="2c8a2-135">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2c8a2-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c8a2-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c8a2-136">CommonParameters</span></span>
<span data-ttu-id="2c8a2-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2c8a2-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c8a2-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c8a2-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c8a2-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2c8a2-139">INPUTS</span></span>

### <span data-ttu-id="2c8a2-140">System. String</span><span class="sxs-lookup"><span data-stu-id="2c8a2-140">System.String</span></span>
<span data-ttu-id="2c8a2-141">System. Int32</span><span class="sxs-lookup"><span data-stu-id="2c8a2-141">System.Int32</span></span>

## <span data-ttu-id="2c8a2-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2c8a2-142">OUTPUTS</span></span>

### <span data-ttu-id="2c8a2-143">System. Object</span><span class="sxs-lookup"><span data-stu-id="2c8a2-143">System.Object</span></span>

## <span data-ttu-id="2c8a2-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2c8a2-144">NOTES</span></span>

## <span data-ttu-id="2c8a2-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2c8a2-145">RELATED LINKS</span></span>

