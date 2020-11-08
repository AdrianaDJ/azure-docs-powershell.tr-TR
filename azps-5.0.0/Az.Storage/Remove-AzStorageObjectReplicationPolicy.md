---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstorageobjectreplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageObjectReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageObjectReplicationPolicy.md
ms.openlocfilehash: 4c42fe6e612f30ab622a0a04498e5474f27690e9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275804"
---
# <span data-ttu-id="6b394-101">Remove-AzStorageObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="6b394-101">Remove-AzStorageObjectReplicationPolicy</span></span>

## <span data-ttu-id="6b394-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b394-102">SYNOPSIS</span></span>
<span data-ttu-id="6b394-103">Belirtilen nesne çoğaltma ilkesini depolama hesabından kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6b394-103">Removes the specified object replication policy from a Storage account.</span></span>

## <span data-ttu-id="6b394-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6b394-104">SYNTAX</span></span>

### <span data-ttu-id="6b394-105">AccountName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6b394-105">AccountName (Default)</span></span>
```
Remove-AzStorageObjectReplicationPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -PolicyId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6b394-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="6b394-106">AccountObject</span></span>
```
Remove-AzStorageObjectReplicationPolicy -StorageAccount <PSStorageAccount> -PolicyId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b394-107">PolicyObject</span><span class="sxs-lookup"><span data-stu-id="6b394-107">PolicyObject</span></span>
```
Remove-AzStorageObjectReplicationPolicy -InputObject <PSObjectReplicationPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b394-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="6b394-108">DESCRIPTION</span></span>
<span data-ttu-id="6b394-109">**Remove-AzStorageObjectReplicationPolicy** cmdlet 'i, belirtilen nesne çoğaltma ilkesini depolama hesabından kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6b394-109">The **Remove-AzStorageObjectReplicationPolicy** cmdlet removes the specified object replication policy from a Storage account.</span></span>

## <span data-ttu-id="6b394-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6b394-110">EXAMPLES</span></span>

### <span data-ttu-id="6b394-111">Örnek 1: bir depolama hesabındaki belirli bir PolicyId ile nesne çoğaltma ilkesini kaldırma.</span><span class="sxs-lookup"><span data-stu-id="6b394-111">Example 1: Remove an object replication policy with specific policyId from a storage account.</span></span>
```
Remove-AzStorageObjectReplicationPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -PolicyId $policyId
```

<span data-ttu-id="6b394-112">Bu komut, bir depolama hesabındaki belirli bir PolicyId ile nesne çoğaltma ilkesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6b394-112">This command removes an object replication policy with specific policyId from a storage account.</span></span>

## <span data-ttu-id="6b394-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6b394-113">PARAMETERS</span></span>

### <span data-ttu-id="6b394-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b394-114">-DefaultProfile</span></span>
<span data-ttu-id="6b394-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6b394-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b394-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6b394-116">-InputObject</span></span>
<span data-ttu-id="6b394-117">Silinecek nesne çoğaltma Ilkesi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="6b394-117">Object Replication Policy object to Delete.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy
Parameter Sets: PolicyObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6b394-118">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="6b394-118">-PassThru</span></span>
<span data-ttu-id="6b394-119">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="6b394-119">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="6b394-120">-PolicyId</span><span class="sxs-lookup"><span data-stu-id="6b394-120">-PolicyId</span></span>
<span data-ttu-id="6b394-121">Nesne çoğaltma Ilkesi kimliği.</span><span class="sxs-lookup"><span data-stu-id="6b394-121">Object Replication Policy Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b394-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b394-122">-ResourceGroupName</span></span>
<span data-ttu-id="6b394-123">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="6b394-123">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b394-124">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="6b394-124">-StorageAccount</span></span>
<span data-ttu-id="6b394-125">Depolama hesabı nesnesi</span><span class="sxs-lookup"><span data-stu-id="6b394-125">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6b394-126">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="6b394-126">-StorageAccountName</span></span>
<span data-ttu-id="6b394-127">Depolama hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="6b394-127">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b394-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="6b394-128">-Confirm</span></span>
<span data-ttu-id="6b394-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6b394-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b394-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b394-130">-WhatIf</span></span>
<span data-ttu-id="6b394-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6b394-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b394-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6b394-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b394-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b394-133">CommonParameters</span></span>
<span data-ttu-id="6b394-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6b394-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b394-135">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b394-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b394-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6b394-136">INPUTS</span></span>

### <span data-ttu-id="6b394-137">Microsoft. Azure. Commands. Management. Storage. model. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6b394-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="6b394-138">Microsoft. Azure. Commands. Management. Storage. model. PSObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="6b394-138">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span></span>

## <span data-ttu-id="6b394-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6b394-139">OUTPUTS</span></span>

### <span data-ttu-id="6b394-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6b394-140">System.Boolean</span></span>

## <span data-ttu-id="6b394-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6b394-141">NOTES</span></span>

## <span data-ttu-id="6b394-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6b394-142">RELATED LINKS</span></span>
