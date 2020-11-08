---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigratenicmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateNicMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateNicMapping.md
ms.openlocfilehash: 118e96747d3859a7b9132747052fb3407b7201ae
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278870"
---
# <span data-ttu-id="d7986-101">New-AzMigrateNicMapping</span><span class="sxs-lookup"><span data-stu-id="d7986-101">New-AzMigrateNicMapping</span></span>

## <span data-ttu-id="d7986-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7986-102">SYNOPSIS</span></span>
<span data-ttu-id="d7986-103">Çoğaltma sunucusunun NIC özelliklerini güncelleştirmek için bir nesne oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d7986-103">Creates an object to update NIC properties of a replicating server.</span></span>

## <span data-ttu-id="d7986-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d7986-104">SYNTAX</span></span>

```
New-AzMigrateNicMapping -NicID <String> [-TargetNicIP <String>] [-TargetNicSelectionType <String>]
 [-TargetNicSubnet <String>] [<CommonParameters>]
```

## <span data-ttu-id="d7986-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d7986-105">DESCRIPTION</span></span>
<span data-ttu-id="d7986-106">New-AzMigrateNicMapping cmdlet 'i geçirilecek sunucuya bağlı kaynak NIC 'in eşlemesini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d7986-106">The New-AzMigrateNicMapping cmdlet creates a mapping of the source NIC attached to the server to be migrated.</span></span>
<span data-ttu-id="d7986-107">Bu nesne, bir çoğaltma sunucusu için NIC 'i ve özelliklerini güncelleştiren Set-AzMigrateServerReplication cmdlet 'e giriş olarak sağlanır.</span><span class="sxs-lookup"><span data-stu-id="d7986-107">This object is provided as an input to the Set-AzMigrateServerReplication cmdlet to update the NIC and its properties for a replicating server.</span></span>

## <span data-ttu-id="d7986-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d7986-108">EXAMPLES</span></span>

### <span data-ttu-id="d7986-109">Örnek 1: NIC nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="d7986-109">Example 1: Create a NIC object</span></span>
```powershell
PS C:\> New-AzMigrateNicMapping -NicID a2399354-653a-464e-a567-d30ef5467a31 -TargetNicSelectionType primary -TargetNicIP "172.17.1.17"

IsPrimaryNic IsSelectedForMigration NicId                                TargetStaticIPAddress TargetSubnetName
------------ ---------------------- -----                                --------------------- ----------------
false        false                  a2399354-653a-464e-a567-d30ef5467a31
```

<span data-ttu-id="d7986-110">Bir NIC güncelleştirme nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d7986-110">Creates a NIC update object.</span></span>

## <span data-ttu-id="d7986-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d7986-111">PARAMETERS</span></span>

### <span data-ttu-id="d7986-112">-NicID</span><span class="sxs-lookup"><span data-stu-id="d7986-112">-NicID</span></span>
<span data-ttu-id="d7986-113">Güncelleştirilecek NIC 'in KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="d7986-113">Specifies the ID of the NIC to be updated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7986-114">-TargetNicIP</span><span class="sxs-lookup"><span data-stu-id="d7986-114">-TargetNicIP</span></span>
<span data-ttu-id="d7986-115">NIC için kullanılacak hedef alt ağda IP 'yi belirtir.</span><span class="sxs-lookup"><span data-stu-id="d7986-115">Specifies the IP within the destination subnet to be used for the NIC.</span></span>

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

### <span data-ttu-id="d7986-116">-TargetNicSelectionType</span><span class="sxs-lookup"><span data-stu-id="d7986-116">-TargetNicSelectionType</span></span>
<span data-ttu-id="d7986-117">Güncelleştirilecek NIC 'in birincil, ikincil veya taşınmadığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d7986-117">Specifies whether the NIC to be updated will be the primary, secondary or not migrated.</span></span>

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

### <span data-ttu-id="d7986-118">-TargetNicSubnet</span><span class="sxs-lookup"><span data-stu-id="d7986-118">-TargetNicSubnet</span></span>
<span data-ttu-id="d7986-119">Hedef sanal ağda, sunucunun geçirilmesi gereken NIC için alt ağ adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d7986-119">Specifies the Subnet name for the NIC in the destination Virtual Network to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="d7986-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7986-120">CommonParameters</span></span>
<span data-ttu-id="d7986-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d7986-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7986-122">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d7986-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7986-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d7986-123">INPUTS</span></span>

## <span data-ttu-id="d7986-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d7986-124">OUTPUTS</span></span>

### <span data-ttu-id="d7986-125">Microsoft. Azure. PowerShell. cmdlet. geçir. modeller. Api20180110. ıvmwarecbtnicınput</span><span class="sxs-lookup"><span data-stu-id="d7986-125">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVMwareCbtNicInput</span></span>

## <span data-ttu-id="d7986-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d7986-126">NOTES</span></span>

<span data-ttu-id="d7986-127">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="d7986-127">ALIASES</span></span>

## <span data-ttu-id="d7986-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d7986-128">RELATED LINKS</span></span>

