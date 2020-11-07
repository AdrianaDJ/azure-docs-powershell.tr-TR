---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricnodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricNodeType.md
ms.openlocfilehash: 2c489a0d041e982b6a870102db73268b7abe5392
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759119"
---
# <span data-ttu-id="89e87-101">Add-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="89e87-101">Add-AzServiceFabricNodeType</span></span>

## <span data-ttu-id="89e87-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89e87-102">SYNOPSIS</span></span>
<span data-ttu-id="89e87-103">Var olan kümeye yeni bir düğüm türü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="89e87-103">Add a new node type to the existing cluster.</span></span>

## <span data-ttu-id="89e87-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="89e87-104">SYNTAX</span></span>

```
Add-AzServiceFabricNodeType [-ResourceGroupName] <String> [-Name] <String> -Capacity <Int32>
 -VmUserName <String> -VmPassword <SecureString> [-VmSku <String>] [-Tier <String>]
 [-DurabilityLevel <DurabilityLevel>] -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89e87-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="89e87-105">DESCRIPTION</span></span>
<span data-ttu-id="89e87-106">Var olan bir kümeye yeni düğüm türü ekleme.</span><span class="sxs-lookup"><span data-stu-id="89e87-106">Add a new node type to a existing cluster.</span></span>

## <span data-ttu-id="89e87-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="89e87-107">EXAMPLES</span></span>

### <span data-ttu-id="89e87-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="89e87-108">Example 1</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String 'Password$123456' -AsPlainText -Force
PS C:\> Add-AzServiceFabricNodeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeType 'n2' -Capacity 5 -VmUserName 'adminName' -VmPassword $pwd
```

<span data-ttu-id="89e87-109">Bu komut, kapasitesi 5 olan ve VM Yöneticisi adı ' adminName ' olan yeni bir NodeType ' N2 '.</span><span class="sxs-lookup"><span data-stu-id="89e87-109">This command will add a new NodeType 'n2' with capacity of 5, and the vm admin name is 'adminName'.</span></span>

## <span data-ttu-id="89e87-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="89e87-110">PARAMETERS</span></span>

### <span data-ttu-id="89e87-111">-Kapasite</span><span class="sxs-lookup"><span data-stu-id="89e87-111">-Capacity</span></span>
<span data-ttu-id="89e87-112">Kapasitede</span><span class="sxs-lookup"><span data-stu-id="89e87-112">Capacity</span></span>

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

### <span data-ttu-id="89e87-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89e87-113">-DefaultProfile</span></span>
<span data-ttu-id="89e87-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="89e87-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89e87-115">-Dur, Itylevel</span><span class="sxs-lookup"><span data-stu-id="89e87-115">-DurabilityLevel</span></span>
<span data-ttu-id="89e87-116">NodeType 'in dayanıklılık düzeyini belirtin.</span><span class="sxs-lookup"><span data-stu-id="89e87-116">Specify the durability level of the NodeType.</span></span>

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

### <span data-ttu-id="89e87-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="89e87-117">-Name</span></span>
<span data-ttu-id="89e87-118">Kümenin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="89e87-118">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="89e87-119">-NodeType</span><span class="sxs-lookup"><span data-stu-id="89e87-119">-NodeType</span></span>
<span data-ttu-id="89e87-120">Düğüm türü adı.</span><span class="sxs-lookup"><span data-stu-id="89e87-120">The node type name.</span></span>

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

### <span data-ttu-id="89e87-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89e87-121">-ResourceGroupName</span></span>
<span data-ttu-id="89e87-122">Kaynak grubunun adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="89e87-122">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="89e87-123">Katmanlı</span><span class="sxs-lookup"><span data-stu-id="89e87-123">-Tier</span></span>
<span data-ttu-id="89e87-124">VM SKU katmanı.</span><span class="sxs-lookup"><span data-stu-id="89e87-124">Vm Sku Tier.</span></span>

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

### <span data-ttu-id="89e87-125">-VmPassword</span><span class="sxs-lookup"><span data-stu-id="89e87-125">-VmPassword</span></span>
<span data-ttu-id="89e87-126">VM 'de oturum açma parolası.</span><span class="sxs-lookup"><span data-stu-id="89e87-126">The password of login to the Vm.</span></span>

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

### <span data-ttu-id="89e87-127">-VmSku</span><span class="sxs-lookup"><span data-stu-id="89e87-127">-VmSku</span></span>
<span data-ttu-id="89e87-128">SKU adı.</span><span class="sxs-lookup"><span data-stu-id="89e87-128">The sku name.</span></span>

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

### <span data-ttu-id="89e87-129">-VmUserName</span><span class="sxs-lookup"><span data-stu-id="89e87-129">-VmUserName</span></span>
<span data-ttu-id="89e87-130">VM için oturum açma Kullanıcı adı.</span><span class="sxs-lookup"><span data-stu-id="89e87-130">The user name for login to Vm.</span></span>

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

### <span data-ttu-id="89e87-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="89e87-131">-Confirm</span></span>
<span data-ttu-id="89e87-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="89e87-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89e87-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89e87-133">-WhatIf</span></span>
<span data-ttu-id="89e87-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="89e87-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="89e87-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="89e87-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89e87-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89e87-136">CommonParameters</span></span>
<span data-ttu-id="89e87-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="89e87-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89e87-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89e87-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89e87-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="89e87-139">INPUTS</span></span>

### <span data-ttu-id="89e87-140">System. String</span><span class="sxs-lookup"><span data-stu-id="89e87-140">System.String</span></span>

### <span data-ttu-id="89e87-141">System. Int32</span><span class="sxs-lookup"><span data-stu-id="89e87-141">System.Int32</span></span>

### <span data-ttu-id="89e87-142">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="89e87-142">System.Security.SecureString</span></span>

### <span data-ttu-id="89e87-143">Microsoft. Azure. Commands. ServiceFabric. modeller. Durkomutlarıdüzey</span><span class="sxs-lookup"><span data-stu-id="89e87-143">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span></span>

## <span data-ttu-id="89e87-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="89e87-144">OUTPUTS</span></span>

### <span data-ttu-id="89e87-145">Microsoft. Azure. Commands. ServiceFabric. modeller. PSCluster</span><span class="sxs-lookup"><span data-stu-id="89e87-145">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="89e87-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="89e87-146">NOTES</span></span>

## <span data-ttu-id="89e87-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="89e87-147">RELATED LINKS</span></span>
