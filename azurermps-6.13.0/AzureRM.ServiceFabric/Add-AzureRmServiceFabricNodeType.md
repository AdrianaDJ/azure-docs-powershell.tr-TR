---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/add-azurermservicefabricnodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricNodeType.md
ms.openlocfilehash: 573dd2f4681ae140fbe98de5d9a7e9df4e2dc764
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589325"
---
# <span data-ttu-id="7c42c-101">Add-AzureRmServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="7c42c-101">Add-AzureRmServiceFabricNodeType</span></span>

## <span data-ttu-id="7c42c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c42c-102">SYNOPSIS</span></span>
<span data-ttu-id="7c42c-103">Var olan kümeye yeni bir düğüm türü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="7c42c-103">Add a new node type to the existing cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7c42c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7c42c-104">SYNTAX</span></span>

```
Add-AzureRmServiceFabricNodeType [-ResourceGroupName] <String> [-Name] <String> -Capacity <Int32>
 -VmUserName <String> -VmPassword <SecureString> [-VmSku <String>] [-Tier <String>]
 [-DurabilityLevel <DurabilityLevel>] -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c42c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7c42c-105">DESCRIPTION</span></span>
<span data-ttu-id="7c42c-106">Var olan bir kümeye yeni düğüm türü ekleme.</span><span class="sxs-lookup"><span data-stu-id="7c42c-106">Add a new node type to a existing cluster.</span></span>

## <span data-ttu-id="7c42c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7c42c-107">EXAMPLES</span></span>

### <span data-ttu-id="7c42c-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7c42c-108">Example 1</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String 'Password$123456' -AsPlainText -Force
PS C:\> Add-AzureRmServiceFabricNodeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeType 'n2' -Capacity 5 -VmUserName 'adminName' -VmPassword $pwd
```

<span data-ttu-id="7c42c-109">Bu komut, kapasitesi 5 olan ve VM Yöneticisi adı ' adminName ' olan yeni bir NodeType ' N2 '.</span><span class="sxs-lookup"><span data-stu-id="7c42c-109">This command will add a new NodeType 'n2' with capacity of 5, and the vm admin name is 'adminName'.</span></span>

## <span data-ttu-id="7c42c-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7c42c-110">PARAMETERS</span></span>

### <span data-ttu-id="7c42c-111">-Kapasite</span><span class="sxs-lookup"><span data-stu-id="7c42c-111">-Capacity</span></span>
<span data-ttu-id="7c42c-112">Kapasitede</span><span class="sxs-lookup"><span data-stu-id="7c42c-112">Capacity</span></span>

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

### <span data-ttu-id="7c42c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c42c-113">-DefaultProfile</span></span>
<span data-ttu-id="7c42c-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7c42c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c42c-115">-Dur, Itylevel</span><span class="sxs-lookup"><span data-stu-id="7c42c-115">-DurabilityLevel</span></span>
<span data-ttu-id="7c42c-116">NodeType 'in dayanıklılık düzeyini belirtin.</span><span class="sxs-lookup"><span data-stu-id="7c42c-116">Specify the durability level of the NodeType.</span></span>

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

### <span data-ttu-id="7c42c-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="7c42c-117">-Name</span></span>
<span data-ttu-id="7c42c-118">Kümenin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="7c42c-118">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="7c42c-119">-NodeType</span><span class="sxs-lookup"><span data-stu-id="7c42c-119">-NodeType</span></span>
<span data-ttu-id="7c42c-120">Düğüm türü adı.</span><span class="sxs-lookup"><span data-stu-id="7c42c-120">The node type name.</span></span>

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

### <span data-ttu-id="7c42c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c42c-121">-ResourceGroupName</span></span>
<span data-ttu-id="7c42c-122">Kaynak grubunun adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="7c42c-122">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="7c42c-123">Katmanlı</span><span class="sxs-lookup"><span data-stu-id="7c42c-123">-Tier</span></span>
<span data-ttu-id="7c42c-124">VM SKU katmanı.</span><span class="sxs-lookup"><span data-stu-id="7c42c-124">Vm Sku Tier.</span></span>

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

### <span data-ttu-id="7c42c-125">-VmPassword</span><span class="sxs-lookup"><span data-stu-id="7c42c-125">-VmPassword</span></span>
<span data-ttu-id="7c42c-126">VM 'de oturum açma parolası.</span><span class="sxs-lookup"><span data-stu-id="7c42c-126">The password of login to the Vm.</span></span>

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

### <span data-ttu-id="7c42c-127">-VmSku</span><span class="sxs-lookup"><span data-stu-id="7c42c-127">-VmSku</span></span>
<span data-ttu-id="7c42c-128">SKU adı.</span><span class="sxs-lookup"><span data-stu-id="7c42c-128">The sku name.</span></span>

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

### <span data-ttu-id="7c42c-129">-VmUserName</span><span class="sxs-lookup"><span data-stu-id="7c42c-129">-VmUserName</span></span>
<span data-ttu-id="7c42c-130">VM için oturum açma Kullanıcı adı.</span><span class="sxs-lookup"><span data-stu-id="7c42c-130">The user name for login to Vm.</span></span>

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

### <span data-ttu-id="7c42c-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="7c42c-131">-Confirm</span></span>
<span data-ttu-id="7c42c-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7c42c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c42c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c42c-133">-WhatIf</span></span>
<span data-ttu-id="7c42c-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7c42c-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7c42c-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7c42c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c42c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c42c-136">CommonParameters</span></span>
<span data-ttu-id="7c42c-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7c42c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c42c-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c42c-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c42c-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7c42c-139">INPUTS</span></span>

### <span data-ttu-id="7c42c-140">System. String</span><span class="sxs-lookup"><span data-stu-id="7c42c-140">System.String</span></span>
<span data-ttu-id="7c42c-141">Parametreler: NodeType (ByValue), katman (ByValue), VmSku (Bydeğeri), VmUserName (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7c42c-141">Parameters: NodeType (ByValue), Tier (ByValue), VmSku (ByValue), VmUserName (ByValue)</span></span>

### <span data-ttu-id="7c42c-142">System. Int32</span><span class="sxs-lookup"><span data-stu-id="7c42c-142">System.Int32</span></span>
<span data-ttu-id="7c42c-143">Parametreler: kapasite (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7c42c-143">Parameters: Capacity (ByValue)</span></span>

### <span data-ttu-id="7c42c-144">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="7c42c-144">System.Security.SecureString</span></span>
<span data-ttu-id="7c42c-145">Parametreler: VmPassword (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7c42c-145">Parameters: VmPassword (ByValue)</span></span>

### <span data-ttu-id="7c42c-146">Microsoft. Azure. Commands. ServiceFabric. modeller. Durkomutlarıdüzey</span><span class="sxs-lookup"><span data-stu-id="7c42c-146">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span></span>
<span data-ttu-id="7c42c-147">Parametreler: Durumitylevel (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7c42c-147">Parameters: DurabilityLevel (ByValue)</span></span>

## <span data-ttu-id="7c42c-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7c42c-148">OUTPUTS</span></span>

### <span data-ttu-id="7c42c-149">Microsoft. Azure. Commands. ServiceFabric. modeller. PSCluster</span><span class="sxs-lookup"><span data-stu-id="7c42c-149">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="7c42c-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7c42c-150">NOTES</span></span>

## <span data-ttu-id="7c42c-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7c42c-151">RELATED LINKS</span></span>
