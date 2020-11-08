---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzDiskEncryptionSet.md
ms.openlocfilehash: 0e95179dcd2b1948b55526f3f2a8bfd5bb1a8834
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268877"
---
# <span data-ttu-id="6e95d-101">Update-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="6e95d-101">Update-AzDiskEncryptionSet</span></span>

## <span data-ttu-id="6e95d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e95d-102">SYNOPSIS</span></span>
<span data-ttu-id="6e95d-103">Disk şifrelemesi kümesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="6e95d-103">Updates a disk encryption set.</span></span>

## <span data-ttu-id="6e95d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6e95d-104">SYNTAX</span></span>

### <span data-ttu-id="6e95d-105">DefaultParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6e95d-105">DefaultParameter (Default)</span></span>
```
Update-AzDiskEncryptionSet [-ResourceGroupName] <String> [-Name] <String> [-KeyUrl <String>]
 [-SourceVaultId <String>] [[-Tag] <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e95d-106">Resourceıdparameter</span><span class="sxs-lookup"><span data-stu-id="6e95d-106">ResourceIdParameter</span></span>
```
Update-AzDiskEncryptionSet [-ResourceId] <String> [-KeyUrl <String>] [-SourceVaultId <String>]
 [[-Tag] <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6e95d-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="6e95d-107">ObjectParameter</span></span>
```
Update-AzDiskEncryptionSet [-InputObject] <PSDiskEncryptionSet> [-KeyUrl <String>] [-SourceVaultId <String>]
 [[-Tag] <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6e95d-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="6e95d-108">DESCRIPTION</span></span>
<span data-ttu-id="6e95d-109">Disk şifrelemesi kümesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="6e95d-109">Updates a disk encryption set.</span></span>

## <span data-ttu-id="6e95d-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6e95d-110">EXAMPLES</span></span>

### <span data-ttu-id="6e95d-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6e95d-111">Example 1</span></span>
```powershell
PS C:\> Update-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -KeyUrl "https://valut1.vault.azure.net:443/keys/key1/mykey" -SourceVaultId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.KeyVault/vaults/vault1;
```

<span data-ttu-id="6e95d-112">Anahtar kasasındaki verilen etkin anahtarı kullanarak disk şifrelemesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="6e95d-112">Updates disk encryption set using the given active key in the key vault.</span></span>

## <span data-ttu-id="6e95d-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6e95d-113">PARAMETERS</span></span>

### <span data-ttu-id="6e95d-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="6e95d-114">-AsJob</span></span>
<span data-ttu-id="6e95d-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="6e95d-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6e95d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e95d-116">-DefaultProfile</span></span>
<span data-ttu-id="6e95d-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6e95d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e95d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6e95d-118">-InputObject</span></span>
<span data-ttu-id="6e95d-119">Disk şifrelemesi kümesinin yerel nesnesi.</span><span class="sxs-lookup"><span data-stu-id="6e95d-119">The local object of the disk encryption set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet
Parameter Sets: ObjectParameter
Aliases: DiskEncryptionSet

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6e95d-120">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="6e95d-120">-KeyUrl</span></span>
<span data-ttu-id="6e95d-121">Tuş Kasası 'ndaki etkin anahtarı gösteren URL</span><span class="sxs-lookup"><span data-stu-id="6e95d-121">Url pointing to the active key in KeyVault</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e95d-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="6e95d-122">-Name</span></span>
<span data-ttu-id="6e95d-123">Disk şifreleme kümesi adı.</span><span class="sxs-lookup"><span data-stu-id="6e95d-123">Name of disk encryption set.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: DiskEncryptionSetName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e95d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e95d-124">-ResourceGroupName</span></span>
<span data-ttu-id="6e95d-125">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6e95d-125">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e95d-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="6e95d-126">-ResourceId</span></span>
<span data-ttu-id="6e95d-127">Kaynağın KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="6e95d-127">The ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e95d-128">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="6e95d-128">-SourceVaultId</span></span>
<span data-ttu-id="6e95d-129">Etkin anahtarı içeren tuş Kasası kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="6e95d-129">Resource id of the KeyVault containing the active key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e95d-130">Etiketli</span><span class="sxs-lookup"><span data-stu-id="6e95d-130">-Tag</span></span>
<span data-ttu-id="6e95d-131">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="6e95d-131">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="6e95d-132">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="6e95d-132">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e95d-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="6e95d-133">-Confirm</span></span>
<span data-ttu-id="6e95d-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6e95d-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e95d-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e95d-135">-WhatIf</span></span>
<span data-ttu-id="6e95d-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6e95d-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e95d-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6e95d-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e95d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e95d-138">CommonParameters</span></span>
<span data-ttu-id="6e95d-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6e95d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e95d-140">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="6e95d-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e95d-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6e95d-141">INPUTS</span></span>

### <span data-ttu-id="6e95d-142">System. String</span><span class="sxs-lookup"><span data-stu-id="6e95d-142">System.String</span></span>

### <span data-ttu-id="6e95d-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSDıskencryptionset</span><span class="sxs-lookup"><span data-stu-id="6e95d-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

### <span data-ttu-id="6e95d-144">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="6e95d-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="6e95d-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6e95d-145">OUTPUTS</span></span>

### <span data-ttu-id="6e95d-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSDıskencryptionset</span><span class="sxs-lookup"><span data-stu-id="6e95d-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="6e95d-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6e95d-147">NOTES</span></span>

## <span data-ttu-id="6e95d-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6e95d-148">RELATED LINKS</span></span>
