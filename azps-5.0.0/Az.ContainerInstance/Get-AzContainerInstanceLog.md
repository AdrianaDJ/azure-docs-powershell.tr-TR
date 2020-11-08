---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerInstance.dll-Help.xml
Module Name: Az.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerinstance/get-azcontainerinstancelog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Get-AzContainerInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Get-AzContainerInstanceLog.md
ms.openlocfilehash: d279e5c08b43640d629e4146faf306d0e85482a8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278724"
---
# <span data-ttu-id="436f9-101">Get-AzContainerInstanceLog</span><span class="sxs-lookup"><span data-stu-id="436f9-101">Get-AzContainerInstanceLog</span></span>

## <span data-ttu-id="436f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="436f9-102">SYNOPSIS</span></span>
<span data-ttu-id="436f9-103">Kapsayıcı grubundaki bir kapsayıcı örneğinin günlüklerini alın.</span><span class="sxs-lookup"><span data-stu-id="436f9-103">Get the logs of a container instance in a container group.</span></span>

## <span data-ttu-id="436f9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="436f9-104">SYNTAX</span></span>

### <span data-ttu-id="436f9-105">Getcontainerınstancelogbynamesparamset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="436f9-105">GetContainerInstanceLogByNamesParamSet (Default)</span></span>
```
Get-AzContainerInstanceLog [-ResourceGroupName] <String> -ContainerGroupName <String> [-Name <String>]
 [-Tail <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="436f9-106">Getcontainerınstancelogbypscontainergroupparamset</span><span class="sxs-lookup"><span data-stu-id="436f9-106">GetContainerInstanceLogByPSContainerGroupParamSet</span></span>
```
Get-AzContainerInstanceLog -InputContainerGroup <PSContainerGroup> [-Name <String>] [-Tail <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="436f9-107">Getcontainerınstancelogbyresourceıdparamset</span><span class="sxs-lookup"><span data-stu-id="436f9-107">GetContainerInstanceLogByResourceIdParamSet</span></span>
```
Get-AzContainerInstanceLog -ResourceId <String> [-Name <String>] [-Tail <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="436f9-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="436f9-108">DESCRIPTION</span></span>
<span data-ttu-id="436f9-109">**Get-AzContainerInstanceLog** cmdlet 'i, kapsayıcı grubundaki bir kapsayıcının günlüklerini alır.</span><span class="sxs-lookup"><span data-stu-id="436f9-109">The **Get-AzContainerInstanceLog** cmdlet gets the logs of a container in a container group.</span></span>

## <span data-ttu-id="436f9-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="436f9-110">EXAMPLES</span></span>

### <span data-ttu-id="436f9-111">Örnek 1: kapsayıcı örneğinin kuyruk günlüğünü alma</span><span class="sxs-lookup"><span data-stu-id="436f9-111">Example 1: Get the tail log of a container instance</span></span>
```
PS C:\> Get-AzContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer -Name container1

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="436f9-112">`container1`Kapsayıcıyı kapsayıcı grubunda alın `mycontainer` .</span><span class="sxs-lookup"><span data-stu-id="436f9-112">Get the log from `container1` in container group `mycontainer`.</span></span> <span data-ttu-id="436f9-113">Varsayılan olarak, en fazla 4MB günlük içeriği döndürür.</span><span class="sxs-lookup"><span data-stu-id="436f9-113">By default, it will return up to 4MB log content.</span></span>

### <span data-ttu-id="436f9-114">Örnek 2: kapsayıcı grubuyla aynı ada sahip bir kapsayıcı örneğinin kuyruk günlüğünü alma</span><span class="sxs-lookup"><span data-stu-id="436f9-114">Example 2: Get the tail log of a container instance that has the same name as the container group</span></span>
```
PS C:\> Get-AzContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="436f9-115">`mycontainer`Kapsayıcıyı kapsayıcı grubunda alın `mycontainer` .</span><span class="sxs-lookup"><span data-stu-id="436f9-115">Get the log from `mycontainer` in container group `mycontainer`.</span></span> <span data-ttu-id="436f9-116">Varsayılan olarak, en fazla 4MB günlük içeriği döndürür.</span><span class="sxs-lookup"><span data-stu-id="436f9-116">By default, it will return up to 4MB log content.</span></span>

### <span data-ttu-id="436f9-117">Örnek 3: kapsayıcı örneğinin günlük dizi 2 satırlarını alma</span><span class="sxs-lookup"><span data-stu-id="436f9-117">Example 3: Get the tail 2 lines of log of a container instance</span></span>
```
PS C:\> Get-AzContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer -Name container1 -Tail 2

Log line 3.
Log line 4.
```

<span data-ttu-id="436f9-118">Konteyner grubunda günlüğün 2 satır sonu alın `container1` `mycontainer` .</span><span class="sxs-lookup"><span data-stu-id="436f9-118">Get the tail 2 lines of log from `container1` in container group `mycontainer`.</span></span>

### <span data-ttu-id="436f9-119">Örnek 4: kapsayıcı grubunda bir kapsayıcı örneğinin kuyruk günlüğünü</span><span class="sxs-lookup"><span data-stu-id="436f9-119">Example 4: Get the tail log of a container instance in a piped in container group</span></span>
```
PS C:\> Get-AzContainerGroup -ResourceGroupName demo -Name mycontainer | Get-AzContainerInstanceLog

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="436f9-120">Konteyner grubunda oturum açma bölümünden oturum açın `mycontainer` `mycontainer` .</span><span class="sxs-lookup"><span data-stu-id="436f9-120">Get the log from `mycontainer` in piped in container group `mycontainer`.</span></span> <span data-ttu-id="436f9-121">Varsayılan olarak, en fazla 4MB günlük içeriği döndürür.</span><span class="sxs-lookup"><span data-stu-id="436f9-121">By default, it will return up to 4MB log content.</span></span>

## <span data-ttu-id="436f9-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="436f9-122">PARAMETERS</span></span>

### <span data-ttu-id="436f9-123">-ContainerGroupName</span><span class="sxs-lookup"><span data-stu-id="436f9-123">-ContainerGroupName</span></span>
<span data-ttu-id="436f9-124">Kapsayıcı grubu adı.</span><span class="sxs-lookup"><span data-stu-id="436f9-124">The container group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetContainerInstanceLogByNamesParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="436f9-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="436f9-125">-DefaultProfile</span></span>
<span data-ttu-id="436f9-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="436f9-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="436f9-127">-Inputcontainergroup</span><span class="sxs-lookup"><span data-stu-id="436f9-127">-InputContainerGroup</span></span>
<span data-ttu-id="436f9-128">Giriş kapsayıcısı Grup nesnesi.</span><span class="sxs-lookup"><span data-stu-id="436f9-128">The input container group object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup
Parameter Sets: GetContainerInstanceLogByPSContainerGroupParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="436f9-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="436f9-129">-Name</span></span>
<span data-ttu-id="436f9-130">Kapsayıcı grubundaki kapsayıcı örneği adı.</span><span class="sxs-lookup"><span data-stu-id="436f9-130">The container instance name in the container group.</span></span>
<span data-ttu-id="436f9-131">Varsayılan: kapsayıcı grubu adıyla aynıdır</span><span class="sxs-lookup"><span data-stu-id="436f9-131">Default: the same as the container group name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="436f9-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="436f9-132">-ResourceGroupName</span></span>
<span data-ttu-id="436f9-133">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="436f9-133">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetContainerInstanceLogByNamesParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="436f9-134">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="436f9-134">-ResourceId</span></span>
<span data-ttu-id="436f9-135">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="436f9-135">The resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetContainerInstanceLogByResourceIdParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="436f9-136">Kuyruklu</span><span class="sxs-lookup"><span data-stu-id="436f9-136">-Tail</span></span>
<span data-ttu-id="436f9-137">Günlükte kuyruk uygulanacak satır sayısı.</span><span class="sxs-lookup"><span data-stu-id="436f9-137">The number of lines to tail the log.</span></span>
<span data-ttu-id="436f9-138">Belirtistemezseniz, cmdlet, 4MB kuyruklu günlük</span><span class="sxs-lookup"><span data-stu-id="436f9-138">If not specify, the cmdlet will return up to 4MB tailed log</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="436f9-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="436f9-139">CommonParameters</span></span>
<span data-ttu-id="436f9-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="436f9-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="436f9-141">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="436f9-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="436f9-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="436f9-142">INPUTS</span></span>

### <span data-ttu-id="436f9-143">Microsoft. Azure. Commands. Containerınstance. modeller. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="436f9-143">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

### <span data-ttu-id="436f9-144">System. String</span><span class="sxs-lookup"><span data-stu-id="436f9-144">System.String</span></span>

## <span data-ttu-id="436f9-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="436f9-145">OUTPUTS</span></span>

### <span data-ttu-id="436f9-146">System. String</span><span class="sxs-lookup"><span data-stu-id="436f9-146">System.String</span></span>

## <span data-ttu-id="436f9-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="436f9-147">NOTES</span></span>

## <span data-ttu-id="436f9-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="436f9-148">RELATED LINKS</span></span>
