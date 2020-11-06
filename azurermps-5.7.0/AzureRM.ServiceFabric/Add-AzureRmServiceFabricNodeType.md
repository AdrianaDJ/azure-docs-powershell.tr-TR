---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/add-azurermservicefabricnodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricNodeType.md
ms.openlocfilehash: 0bae150e60332e4f1bb0ee4f2ee67699c13eb5e7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587438"
---
# <span data-ttu-id="b22d0-101">Add-AzureRmServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="b22d0-101">Add-AzureRmServiceFabricNodeType</span></span>

## <span data-ttu-id="b22d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b22d0-102">SYNOPSIS</span></span>
<span data-ttu-id="b22d0-103">Var olan kümeye yeni bir düğüm türü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="b22d0-103">Add a new node type to the existing cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b22d0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b22d0-104">SYNTAX</span></span>

```
Add-AzureRmServiceFabricNodeType [-ResourceGroupName] <String> [-Name] <String> -Capacity <Int32>
 -VmUserName <String> -VmPassword <SecureString> [-VmSku <String>] [-Tier <String>]
 [-DurabilityLevel <DurabilityLevel>] -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b22d0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b22d0-105">DESCRIPTION</span></span>
<span data-ttu-id="b22d0-106">Var olan bir kümeye yeni düğüm türü ekleme.</span><span class="sxs-lookup"><span data-stu-id="b22d0-106">Add a new node type to a existing cluster.</span></span>

## <span data-ttu-id="b22d0-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b22d0-107">EXAMPLES</span></span>

### <span data-ttu-id="b22d0-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b22d0-108">Example 1</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String 'Password$123456' -AsPlainText -Force
PS C:\> Add-AzureRmServiceFabricNodeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeType 'n2' -Capacity 5 -VmUserName 'adminName' -VmPassword $pwd
```

<span data-ttu-id="b22d0-109">Bu komut, kapasitesi 5 olan ve VM Yöneticisi adı ' adminName ' olan yeni bir NodeType ' N2 '.</span><span class="sxs-lookup"><span data-stu-id="b22d0-109">This command will add a new NodeType 'n2' with capacity of 5, and the vm admin name is 'adminName'.</span></span>

## <span data-ttu-id="b22d0-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b22d0-110">PARAMETERS</span></span>

### <span data-ttu-id="b22d0-111">-Kapasite</span><span class="sxs-lookup"><span data-stu-id="b22d0-111">-Capacity</span></span>
<span data-ttu-id="b22d0-112">Kapasitede</span><span class="sxs-lookup"><span data-stu-id="b22d0-112">Capacity</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b22d0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b22d0-113">-DefaultProfile</span></span>
<span data-ttu-id="b22d0-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b22d0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b22d0-115">-Dur, Itylevel</span><span class="sxs-lookup"><span data-stu-id="b22d0-115">-DurabilityLevel</span></span>
<span data-ttu-id="b22d0-116">NodeType 'in dayanıklılık düzeyini belirtin.</span><span class="sxs-lookup"><span data-stu-id="b22d0-116">Specify the durability level of the NodeType.</span></span>

```yaml
Type: DurabilityLevel
Parameter Sets: (All)
Aliases: 
Accepted values: Bronze, Silver, Gold

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b22d0-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="b22d0-117">-Name</span></span>
<span data-ttu-id="b22d0-118">Kümenin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="b22d0-118">Specify the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b22d0-119">-NodeType</span><span class="sxs-lookup"><span data-stu-id="b22d0-119">-NodeType</span></span>
<span data-ttu-id="b22d0-120">Düğüm türü adı.</span><span class="sxs-lookup"><span data-stu-id="b22d0-120">The node type name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b22d0-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b22d0-121">-ResourceGroupName</span></span>
<span data-ttu-id="b22d0-122">Kaynak grubunun adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="b22d0-122">Specify the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b22d0-123">Katmanlı</span><span class="sxs-lookup"><span data-stu-id="b22d0-123">-Tier</span></span>
<span data-ttu-id="b22d0-124">VM SKU katmanı.</span><span class="sxs-lookup"><span data-stu-id="b22d0-124">Vm Sku Tier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b22d0-125">-VmPassword</span><span class="sxs-lookup"><span data-stu-id="b22d0-125">-VmPassword</span></span>
<span data-ttu-id="b22d0-126">VM 'de oturum açma parolası.</span><span class="sxs-lookup"><span data-stu-id="b22d0-126">The password of login to the Vm.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b22d0-127">-VmSku</span><span class="sxs-lookup"><span data-stu-id="b22d0-127">-VmSku</span></span>
<span data-ttu-id="b22d0-128">SKU adı.</span><span class="sxs-lookup"><span data-stu-id="b22d0-128">The sku name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b22d0-129">-VmUserName</span><span class="sxs-lookup"><span data-stu-id="b22d0-129">-VmUserName</span></span>
<span data-ttu-id="b22d0-130">VM için oturum açma Kullanıcı adı.</span><span class="sxs-lookup"><span data-stu-id="b22d0-130">The user name for login to Vm.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b22d0-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="b22d0-131">-Confirm</span></span>
<span data-ttu-id="b22d0-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b22d0-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b22d0-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b22d0-133">-WhatIf</span></span>
<span data-ttu-id="b22d0-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b22d0-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b22d0-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b22d0-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b22d0-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b22d0-136">CommonParameters</span></span>
<span data-ttu-id="b22d0-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b22d0-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b22d0-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b22d0-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b22d0-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b22d0-139">INPUTS</span></span>

### <span data-ttu-id="b22d0-140">System. String</span><span class="sxs-lookup"><span data-stu-id="b22d0-140">System.String</span></span>
<span data-ttu-id="b22d0-141">System. Int32</span><span class="sxs-lookup"><span data-stu-id="b22d0-141">System.Int32</span></span>

## <span data-ttu-id="b22d0-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b22d0-142">OUTPUTS</span></span>

### <span data-ttu-id="b22d0-143">System. Object</span><span class="sxs-lookup"><span data-stu-id="b22d0-143">System.Object</span></span>

## <span data-ttu-id="b22d0-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b22d0-144">NOTES</span></span>

## <span data-ttu-id="b22d0-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b22d0-145">RELATED LINKS</span></span>

