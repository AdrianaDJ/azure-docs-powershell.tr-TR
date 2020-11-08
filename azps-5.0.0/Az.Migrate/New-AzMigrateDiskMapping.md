---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigratediskmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateDiskMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateDiskMapping.md
ms.openlocfilehash: 812b1a3de090240a306f3d0a5b768ce25f3b22e5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278869"
---
# <span data-ttu-id="2ff46-101">New-AzMigrateDiskMapping</span><span class="sxs-lookup"><span data-stu-id="2ff46-101">New-AzMigrateDiskMapping</span></span>

## <span data-ttu-id="2ff46-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ff46-102">SYNOPSIS</span></span>
<span data-ttu-id="2ff46-103">Yeni bir disk eşlemesi oluşturur</span><span class="sxs-lookup"><span data-stu-id="2ff46-103">Creates a new disk mapping</span></span>

## <span data-ttu-id="2ff46-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2ff46-104">SYNTAX</span></span>

```
New-AzMigrateDiskMapping -DiskID <String> -DiskType <DiskAccountType> -IsOSDisk <String>
 [-DiskEncryptionSetID <String>] [<CommonParameters>]
```

## <span data-ttu-id="2ff46-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2ff46-105">DESCRIPTION</span></span>
<span data-ttu-id="2ff46-106">New-AzMigrateDiskMapping cmdlet 'i geçirilecek sunucuya bağlı kaynak diskin eşlemesini oluşturur</span><span class="sxs-lookup"><span data-stu-id="2ff46-106">The New-AzMigrateDiskMapping cmdlet creates a mapping of the source disk attached to the server to be migrated</span></span>

## <span data-ttu-id="2ff46-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2ff46-107">EXAMPLES</span></span>

### <span data-ttu-id="2ff46-108">Örnek 1: diskleri yapma</span><span class="sxs-lookup"><span data-stu-id="2ff46-108">Example 1: Make disks</span></span>
```powershell
PS C:\> New-AzMigrateDiskMapping -DiskID a -DiskType Standard -IsOSDisk 'true'

DiskEncryptionSetId DiskId   DiskType  IsOSDisk LogStorageAccountId LogStorageAccountSasSecretName  
------------------- ------   --------  -------- ------------------- ------------------------------   
                      a      Standard  true  
```

<span data-ttu-id="2ff46-109">New-AzMigrateServerReplication giriş sağlamak için disk nesnesini alın</span><span class="sxs-lookup"><span data-stu-id="2ff46-109">Get disks object to provide input for New-AzMigrateServerReplication</span></span>

## <span data-ttu-id="2ff46-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2ff46-110">PARAMETERS</span></span>

### <span data-ttu-id="2ff46-111">-DiskEncryptionSetID</span><span class="sxs-lookup"><span data-stu-id="2ff46-111">-DiskEncryptionSetID</span></span>
<span data-ttu-id="2ff46-112">Kullanılacak disk şifrelemesi kümesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2ff46-112">Specifies the disk encyption set to be used.</span></span>

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

### <span data-ttu-id="2ff46-113">-DiskID</span><span class="sxs-lookup"><span data-stu-id="2ff46-113">-DiskID</span></span>
<span data-ttu-id="2ff46-114">Yükseltilecek olan sunucuya bağlı diskin disk KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="2ff46-114">Specifies the disk ID of the disk attached to the discovered server to be migrated.</span></span>

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

### <span data-ttu-id="2ff46-115">-DiskType</span><span class="sxs-lookup"><span data-stu-id="2ff46-115">-DiskType</span></span>
<span data-ttu-id="2ff46-116">Azure VM için kullanılacak disk türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="2ff46-116">Specifies the type of disks to be used for the Azure VM.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Support.DiskAccountType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ff46-117">-Isosdisk</span><span class="sxs-lookup"><span data-stu-id="2ff46-117">-IsOSDisk</span></span>
<span data-ttu-id="2ff46-118">Diske geçirilecek kaynak sunucunun Işletim sistemini içerip içermediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2ff46-118">Specifies whether the disk contains the Operating System for the source server to be migrated.</span></span>

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

### <span data-ttu-id="2ff46-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ff46-119">CommonParameters</span></span>
<span data-ttu-id="2ff46-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2ff46-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ff46-121">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="2ff46-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ff46-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2ff46-122">INPUTS</span></span>

## <span data-ttu-id="2ff46-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2ff46-123">OUTPUTS</span></span>

### <span data-ttu-id="2ff46-124">Microsoft. Azure. PowerShell. cmdlet. geçir. modeller. Api20180110. ıvmwarecbtdiskınput</span><span class="sxs-lookup"><span data-stu-id="2ff46-124">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVMwareCbtDiskInput</span></span>

## <span data-ttu-id="2ff46-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2ff46-125">NOTES</span></span>

<span data-ttu-id="2ff46-126">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="2ff46-126">ALIASES</span></span>

## <span data-ttu-id="2ff46-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2ff46-127">RELATED LINKS</span></span>

