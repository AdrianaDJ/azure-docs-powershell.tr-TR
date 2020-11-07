---
external help file: Microsoft.Azure.Commands.ContainerInstance.dll-Help.xml
Module Name: AzureRM.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerinstance/get-azurermcontainerinstancelog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/Get-AzureRmContainerInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/Get-AzureRmContainerInstanceLog.md
ms.openlocfilehash: 08a4ab0f0d937f06ee0ac958aa57a2f0eed5e4a3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93761978"
---
# <span data-ttu-id="ae25f-101">Get-AzureRmContainerInstanceLog</span><span class="sxs-lookup"><span data-stu-id="ae25f-101">Get-AzureRmContainerInstanceLog</span></span>

## <span data-ttu-id="ae25f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae25f-102">SYNOPSIS</span></span>
<span data-ttu-id="ae25f-103">Kapsayıcı grubundaki bir kapsayıcı örneğinin günlüklerini alın.</span><span class="sxs-lookup"><span data-stu-id="ae25f-103">Get the logs of a container instance in a container group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae25f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ae25f-104">SYNTAX</span></span>

### <span data-ttu-id="ae25f-105">Getcontainerınstancelogbynamesparamset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ae25f-105">GetContainerInstanceLogByNamesParamSet (Default)</span></span>
```
Get-AzureRmContainerInstanceLog [-ResourceGroupName] <String> -ContainerGroupName <String> [-Name <String>]
 [-Tail <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae25f-106">Getcontainerınstancelogbypscontainergroupparamset</span><span class="sxs-lookup"><span data-stu-id="ae25f-106">GetContainerInstanceLogByPSContainerGroupParamSet</span></span>
```
Get-AzureRmContainerInstanceLog -InputContainerGroup <PSContainerGroup> [-Name <String>] [-Tail <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae25f-107">Getcontainerınstancelogbyresourceıdparamset</span><span class="sxs-lookup"><span data-stu-id="ae25f-107">GetContainerInstanceLogByResourceIdParamSet</span></span>
```
Get-AzureRmContainerInstanceLog -ResourceId <String> [-Name <String>] [-Tail <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae25f-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="ae25f-108">DESCRIPTION</span></span>
<span data-ttu-id="ae25f-109">**Get-AzureRmContainerInstanceLog** cmdlet 'i, kapsayıcı grubundaki bir kapsayıcının günlüklerini alır.</span><span class="sxs-lookup"><span data-stu-id="ae25f-109">The **Get-AzureRmContainerInstanceLog** cmdlet gets the logs of a container in a container group.</span></span>

## <span data-ttu-id="ae25f-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ae25f-110">EXAMPLES</span></span>

### <span data-ttu-id="ae25f-111">Örnek 1: kapsayıcı örneğinin kuyruk günlüğünü alma</span><span class="sxs-lookup"><span data-stu-id="ae25f-111">Example 1: Get the tail log of a container instance</span></span>
```
PS C:\> Get-AzureRmContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer -Name container1

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="ae25f-112">`container1`Kapsayıcıyı kapsayıcı grubunda alın `mycontainer` .</span><span class="sxs-lookup"><span data-stu-id="ae25f-112">Get the log from `container1` in container group `mycontainer`.</span></span> <span data-ttu-id="ae25f-113">Varsayılan olarak, en fazla 4MB günlük içeriği döndürür.</span><span class="sxs-lookup"><span data-stu-id="ae25f-113">By default, it will return up to 4MB log content.</span></span>

### <span data-ttu-id="ae25f-114">Örnek 2: kapsayıcı grubuyla aynı ada sahip bir kapsayıcı örneğinin kuyruk günlüğünü alma</span><span class="sxs-lookup"><span data-stu-id="ae25f-114">Example 2: Get the tail log of a container instance that has the same name as the container group</span></span>
```
PS C:\> Get-AzureRmContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="ae25f-115">`mycontainer`Kapsayıcıyı kapsayıcı grubunda alın `mycontainer` .</span><span class="sxs-lookup"><span data-stu-id="ae25f-115">Get the log from `mycontainer` in container group `mycontainer`.</span></span> <span data-ttu-id="ae25f-116">Varsayılan olarak, en fazla 4MB günlük içeriği döndürür.</span><span class="sxs-lookup"><span data-stu-id="ae25f-116">By default, it will return up to 4MB log content.</span></span>

### <span data-ttu-id="ae25f-117">Örnek 3: kapsayıcı örneğinin günlük dizi 2 satırlarını alma</span><span class="sxs-lookup"><span data-stu-id="ae25f-117">Example 3: Get the tail 2 lines of log of a container instance</span></span>
```
PS C:\> Get-AzureRmContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer -Name container1 -Tail 2

Log line 3.
Log line 4.
```

<span data-ttu-id="ae25f-118">Konteyner grubunda günlüğün 2 satır sonu alın `container1` `mycontainer` .</span><span class="sxs-lookup"><span data-stu-id="ae25f-118">Get the tail 2 lines of log from `container1` in container group `mycontainer`.</span></span>

### <span data-ttu-id="ae25f-119">Örnek 4: kapsayıcı grubunda bir kapsayıcı örneğinin kuyruk günlüğünü</span><span class="sxs-lookup"><span data-stu-id="ae25f-119">Example 4: Get the tail log of a container instance in a piped in container group</span></span>
```
PS C:\> Get-AzureRmContainerGroup -ResourceGroupName demo -Name mycontainer | Get-AzureRmContainerInstanceLog

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="ae25f-120">Konteyner grubunda oturum açma bölümünden oturum açın `mycontainer` `mycontainer` .</span><span class="sxs-lookup"><span data-stu-id="ae25f-120">Get the log from `mycontainer` in piped in container group `mycontainer`.</span></span> <span data-ttu-id="ae25f-121">Varsayılan olarak, en fazla 4MB günlük içeriği döndürür.</span><span class="sxs-lookup"><span data-stu-id="ae25f-121">By default, it will return up to 4MB log content.</span></span>

## <span data-ttu-id="ae25f-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ae25f-122">PARAMETERS</span></span>

### <span data-ttu-id="ae25f-123">-ContainerGroupName</span><span class="sxs-lookup"><span data-stu-id="ae25f-123">-ContainerGroupName</span></span>
<span data-ttu-id="ae25f-124">Kapsayıcı grubu adı.</span><span class="sxs-lookup"><span data-stu-id="ae25f-124">The container group name.</span></span>

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

### <span data-ttu-id="ae25f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae25f-125">-DefaultProfile</span></span>
<span data-ttu-id="ae25f-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ae25f-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae25f-127">-Inputcontainergroup</span><span class="sxs-lookup"><span data-stu-id="ae25f-127">-InputContainerGroup</span></span>
<span data-ttu-id="ae25f-128">Giriş kapsayıcısı Grup nesnesi.</span><span class="sxs-lookup"><span data-stu-id="ae25f-128">The input container group object.</span></span>

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

### <span data-ttu-id="ae25f-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="ae25f-129">-Name</span></span>
<span data-ttu-id="ae25f-130">Kapsayıcı grubundaki kapsayıcı örneği adı.</span><span class="sxs-lookup"><span data-stu-id="ae25f-130">The container instance name in the container group.</span></span>
<span data-ttu-id="ae25f-131">Varsayılan: kapsayıcı grubu adıyla aynıdır</span><span class="sxs-lookup"><span data-stu-id="ae25f-131">Default: the same as the container group name</span></span>

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

### <span data-ttu-id="ae25f-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae25f-132">-ResourceGroupName</span></span>
<span data-ttu-id="ae25f-133">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="ae25f-133">The resource group name.</span></span>

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

### <span data-ttu-id="ae25f-134">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="ae25f-134">-ResourceId</span></span>
<span data-ttu-id="ae25f-135">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="ae25f-135">The resource id.</span></span>

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

### <span data-ttu-id="ae25f-136">Kuyruklu</span><span class="sxs-lookup"><span data-stu-id="ae25f-136">-Tail</span></span>
<span data-ttu-id="ae25f-137">Günlükte kuyruk uygulanacak satır sayısı.</span><span class="sxs-lookup"><span data-stu-id="ae25f-137">The number of lines to tail the log.</span></span>
<span data-ttu-id="ae25f-138">Belirtistemezseniz, cmdlet, 4MB kuyruklu günlük</span><span class="sxs-lookup"><span data-stu-id="ae25f-138">If not specify, the cmdlet will return up to 4MB tailed log</span></span>

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

### <span data-ttu-id="ae25f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae25f-139">CommonParameters</span></span>
<span data-ttu-id="ae25f-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ae25f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae25f-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae25f-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae25f-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ae25f-142">INPUTS</span></span>

### <span data-ttu-id="ae25f-143">Microsoft. Azure. Commands. Containerınstance. modeller. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="ae25f-143">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>
<span data-ttu-id="ae25f-144">Parametreler: ınputcontainergroup (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ae25f-144">Parameters: InputContainerGroup (ByValue)</span></span>

### <span data-ttu-id="ae25f-145">System. String</span><span class="sxs-lookup"><span data-stu-id="ae25f-145">System.String</span></span>

## <span data-ttu-id="ae25f-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ae25f-146">OUTPUTS</span></span>

### <span data-ttu-id="ae25f-147">System. String</span><span class="sxs-lookup"><span data-stu-id="ae25f-147">System.String</span></span>

## <span data-ttu-id="ae25f-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ae25f-148">NOTES</span></span>

## <span data-ttu-id="ae25f-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ae25f-149">RELATED LINKS</span></span>
