---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskencryptionsetconfig.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSetConfig.md
ms.openlocfilehash: 5d38a1104d1f2d1f569560027c540a2c8605bdae
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096945"
---
# <span data-ttu-id="a3db3-101">New-AzDiskEncryptionSetConfig</span><span class="sxs-lookup"><span data-stu-id="a3db3-101">New-AzDiskEncryptionSetConfig</span></span>

## <span data-ttu-id="a3db3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3db3-102">SYNOPSIS</span></span>
<span data-ttu-id="a3db3-103">Yapılandırılabilir bir disk şifrelemesi kümesi nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a3db3-103">Creates a configurable disk encryption set object.</span></span>

## <span data-ttu-id="a3db3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a3db3-104">SYNTAX</span></span>

```
New-AzDiskEncryptionSetConfig [-Location] <String> [[-Tag] <Hashtable>] [[-IdentityType] <String>]
 [[-SourceVaultId] <String>] [-KeyUrl <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a3db3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a3db3-105">DESCRIPTION</span></span>
<span data-ttu-id="a3db3-106">Yapılandırılabilir bir disk şifrelemesi kümesi nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a3db3-106">Creates a configurable disk encryption set object.</span></span>

## <span data-ttu-id="a3db3-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a3db3-107">EXAMPLES</span></span>

### <span data-ttu-id="a3db3-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a3db3-108">Example 1</span></span>
```powershell
PS C:\> $config = New-AzDiskEncryptionSetConfig -Location 'westcentralus' -KeyUrl "https://valut1.vault.azure.net:443/keys/key1/mykey" -SourceVaultId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.KeyVault/vaults/vault1 -IdentityType 'SystemAssigned'
PS C:\> New-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -DiskEncryptionSet $config;
```

<span data-ttu-id="a3db3-109">Anahtar kasasındaki verilen etkin anahtarı kullanarak disk şifrelemesi kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a3db3-109">Creates disk encryption set using the given active key in the key vault.</span></span>

## <span data-ttu-id="a3db3-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a3db3-110">PARAMETERS</span></span>

### <span data-ttu-id="a3db3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3db3-111">-DefaultProfile</span></span>
<span data-ttu-id="a3db3-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a3db3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3db3-113">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="a3db3-113">-IdentityType</span></span>
<span data-ttu-id="a3db3-114">DiskEncryptionSet tarafından kullanılan yönetilen kimliğin türü.</span><span class="sxs-lookup"><span data-stu-id="a3db3-114">The type of Managed Identity used by the DiskEncryptionSet.</span></span> <span data-ttu-id="a3db3-115">Yalnızca SystemAssigned destekleniyor.</span><span class="sxs-lookup"><span data-stu-id="a3db3-115">Only SystemAssigned is supported.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3db3-116">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="a3db3-116">-KeyUrl</span></span>
<span data-ttu-id="a3db3-117">Tuş Kasası 'ndaki etkin anahtarı gösteren URL</span><span class="sxs-lookup"><span data-stu-id="a3db3-117">Url pointing to the active key in KeyVault</span></span>

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

### <span data-ttu-id="a3db3-118">-Konum</span><span class="sxs-lookup"><span data-stu-id="a3db3-118">-Location</span></span>
<span data-ttu-id="a3db3-119">Bir konum belirtir.</span><span class="sxs-lookup"><span data-stu-id="a3db3-119">Specifies a location.</span></span>

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

### <span data-ttu-id="a3db3-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="a3db3-120">-SourceVaultId</span></span>
<span data-ttu-id="a3db3-121">Etkin anahtarı içeren tuş Kasası kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="a3db3-121">Resource id of the KeyVault containing the active key.</span></span>

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

### <span data-ttu-id="a3db3-122">Etiketli</span><span class="sxs-lookup"><span data-stu-id="a3db3-122">-Tag</span></span>
<span data-ttu-id="a3db3-123">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="a3db3-123">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="a3db3-124">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="a3db3-124">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="a3db3-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="a3db3-125">-Confirm</span></span>
<span data-ttu-id="a3db3-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a3db3-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3db3-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3db3-127">-WhatIf</span></span>
<span data-ttu-id="a3db3-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a3db3-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3db3-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a3db3-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3db3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3db3-130">CommonParameters</span></span>
<span data-ttu-id="a3db3-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a3db3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3db3-132">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a3db3-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3db3-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a3db3-133">INPUTS</span></span>

### <span data-ttu-id="a3db3-134">System. String</span><span class="sxs-lookup"><span data-stu-id="a3db3-134">System.String</span></span>

### <span data-ttu-id="a3db3-135">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="a3db3-135">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a3db3-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a3db3-136">OUTPUTS</span></span>

### <span data-ttu-id="a3db3-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSDıskencryptionset</span><span class="sxs-lookup"><span data-stu-id="a3db3-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="a3db3-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a3db3-138">NOTES</span></span>

## <span data-ttu-id="a3db3-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a3db3-139">RELATED LINKS</span></span>
