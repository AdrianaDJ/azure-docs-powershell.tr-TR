---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azdatalakegen2itemaclobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzDataLakeGen2ItemACLObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzDataLakeGen2ItemACLObject.md
ms.openlocfilehash: d16a476bea988afb53ddff7b34a83658e0f274e1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096705"
---
# <span data-ttu-id="9272c-101">Set-AzDataLakeGen2ItemAclObject</span><span class="sxs-lookup"><span data-stu-id="9272c-101">Set-AzDataLakeGen2ItemAclObject</span></span>

## <span data-ttu-id="9272c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9272c-102">SYNOPSIS</span></span>
<span data-ttu-id="9272c-103">Update-AzDataLakeGen2Item cmdlet 'te kullanılabilen bir DataLake Gen2 Item ACL nesnesi oluşturur/güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="9272c-103">Creates/Updates a DataLake gen2 item ACL object, which can be used in Update-AzDataLakeGen2Item cmdlet.</span></span>

## <span data-ttu-id="9272c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9272c-104">SYNTAX</span></span>

```
Set-AzDataLakeGen2ItemAclObject [-EntityId <String>] [-DefaultScope] -Permission <String>
 [-InputObject <PSPathAccessControlEntry[]>] -AccessControlType <AccessControlType> [<CommonParameters>]
```

## <span data-ttu-id="9272c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9272c-105">DESCRIPTION</span></span>
<span data-ttu-id="9272c-106">**Set-AzDataLakeGen2ItemAclObject** cmdlet 'i, Update-AzDataLakeGen2Item cmdlet 'te kullanılabilen bir datalake Gen2 Item ACL nesnesi oluşturur/güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="9272c-106">The **Set-AzDataLakeGen2ItemAclObject** cmdlet creates/updates a DataLake gen2 item ACL object, which can be used in Update-AzDataLakeGen2Item cmdlet.</span></span>
<span data-ttu-id="9272c-107">Giriş ACL 'de aynı AccessControlType/EntityId/DefaultScope içeren yeni ACL girişi yoksa, yeni bir ACL girişi oluşturur, başka bir ACL girdisi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9272c-107">If the new ACL entry with same AccessControlType/EntityId/DefaultScope not exist in the input ACL, will create a new ACL entry, else update permission of existing ACL entry.</span></span>

## <span data-ttu-id="9272c-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9272c-108">EXAMPLES</span></span>

### <span data-ttu-id="9272c-109">Örnek 1:3 ACL girişi olan bir ACL nesnesi oluşturma ve bir dizindeki ACL 'yi güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="9272c-109">Example 1: Create an ACL object with 3 ACL entry, and update ACL on a directory</span></span>
```
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -Permission rwx -DefaultScope
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType group -Permission rw- -InputObject $acl 
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType other -Permission "rw-" -InputObject $acl
PS C:\>Update-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/dir3" -ACL $acl

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/dir3            True                         2020-03-23 09:34:31Z rwxrw-rw-+   $superuser           $superuser
```

<span data-ttu-id="9272c-110">Bu komut, 3 ACL girişi içeren bir ACL nesnesi oluşturur (var olan ACL nesnesine ACL girişi eklemek için-InputObject parametresini kullanın) ve bir dizindeki ACL 'yi günceller.</span><span class="sxs-lookup"><span data-stu-id="9272c-110">This command creates an ACL object with 3 ACL entries (use -InputObject parameter to add acl entry to existing acl object), and updates ACL on a directory.</span></span>

### <span data-ttu-id="9272c-111">Örnek 2:4 ACL girişi olan bir ACL nesnesi oluşturma ve var olan ACL girdisinin izinlerini güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="9272c-111">Example 2: Create an ACL object with 4 ACL entries, and update permission of an existing ACL entry</span></span>
```
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -Permission rwx -DefaultScope
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType group -Permission rw- -InputObject $acl 
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType other -Permission "rw-" -InputObject $acl
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -EntityId $id -Permission rwx -InputObject $acl 
PS C:\>$acl

DefaultScope AccessControlType EntityId                             Permissions
------------ ----------------- --------                             -----------
True         User                                                   rwx        
False        Group                                                  rw-        
False        Other                                                  rw-        
False        User              ********-****-****-****-************ rwx        

PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -EntityId $id -Permission r-x -InputObject $acl 
PS C:\>$acl  

DefaultScope AccessControlType EntityId                             Permissions
------------ ----------------- --------                             -----------
True         User                                                   rwx        
False        Group                                                  rw-        
False        Other                                                  rw-        
False        User              ********-****-****-****-************ r-x
```

<span data-ttu-id="9272c-112">Bu komut ilk olarak 4 ACL girişi olan bir ACL nesnesi oluşturur, ardından cmdlet 'i farklı izinlerle, var olan bir ACL girdisinin aynı AccessControlType/EntityId/DefaultScope değeriyle yeniden çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="9272c-112">This command first creates an ACL object with 4 ACL entries, then run the cmdlet again with different permission but same AccessControlType/EntityId/DefaultScope of an existing ACL entry.</span></span>
<span data-ttu-id="9272c-113">Ardından ACL girdisinin izni güncellenir, ancak yeni bir ACL girdisi eklenmez.</span><span class="sxs-lookup"><span data-stu-id="9272c-113">Then the permission of the ACL entry is updated, but no new ACL entry is added.</span></span>

## <span data-ttu-id="9272c-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9272c-114">PARAMETERS</span></span>

### <span data-ttu-id="9272c-115">-AccessControlType</span><span class="sxs-lookup"><span data-stu-id="9272c-115">-AccessControlType</span></span>
<span data-ttu-id="9272c-116">Dört tür vardır: "Kullanıcı" sahibi veya adlandırılmış bir kullanıcıya hak veriyor, "Grup" sahibi olan gruba veya adlandırılmış bir gruba hak veriyor, "maske" adlandırılmış kullanıcılara ve grupların üyelerine verilen hakları kısıtlar ve "diğer" diğer girdilerde bulunmayan tüm kullanıcılara hak veriyor.</span><span class="sxs-lookup"><span data-stu-id="9272c-116">There are four types: "user" grants rights to the owner or a named user, "group" grants rights to the owning group or a named group, "mask" restricts rights granted to named users and the members of groups, and "other" grants rights to all users not found in any of the other entries.</span></span>

```yaml
Type: Azure.Storage.Files.DataLake.Models.AccessControlType
Parameter Sets: (All)
Aliases:
Accepted values: User, Group, Mask, Other

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9272c-117">-DefaultScope</span><span class="sxs-lookup"><span data-stu-id="9272c-117">-DefaultScope</span></span>
<span data-ttu-id="9272c-118">ACE 'nin bir dizinin varsayılan ACL 'ye ait olduğunu belirtmek için bu parametreyi ayarlayın; Yoksa kapsam örtük ve ACE Access ACL 'ye aittir.</span><span class="sxs-lookup"><span data-stu-id="9272c-118">Set this parameter to indicate the ACE belongs to the default ACL for a directory; otherwise scope is implicit and the ACE belongs to the access ACL.</span></span>

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

### <span data-ttu-id="9272c-119">-EntityId</span><span class="sxs-lookup"><span data-stu-id="9272c-119">-EntityId</span></span>
<span data-ttu-id="9272c-120">Kullanıcı veya grup tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="9272c-120">The user or group identifier.</span></span>
<span data-ttu-id="9272c-121">AccessControlType "Mask" ve "diğer" girdileri için kullanılmaz.</span><span class="sxs-lookup"><span data-stu-id="9272c-121">It is omitted for entries of AccessControlType "mask" and "other".</span></span>
<span data-ttu-id="9272c-122">Kullanıcı veya grup kimliği sahibi ve sahip olan grup için de atlandı.</span><span class="sxs-lookup"><span data-stu-id="9272c-122">The user or group identifier is also omitted for the owner and owning group.</span></span>

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

### <span data-ttu-id="9272c-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9272c-123">-InputObject</span></span>
<span data-ttu-id="9272c-124">PSPathAccessControlEntry \[ \] nesnesiyle karşılaşırsanız yeni ACL 'Yi, PSPathAccessControlEntry nesnesinin yeni bir öğesi olarak ekler \[ \] .</span><span class="sxs-lookup"><span data-stu-id="9272c-124">If input the PSPathAccessControlEntry\[\] object, will add the new ACL as a new element of the input PSPathAccessControlEntry\[\] object.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSPathAccessControlEntry[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9272c-125">-İzin</span><span class="sxs-lookup"><span data-stu-id="9272c-125">-Permission</span></span>
<span data-ttu-id="9272c-126">İzin alanı, ilk karakterin ' r ' olduğu bir 3 karakterlik dizi olduğundan, okuma erişimi vermek için ikinci karakter ' w ' olur ve yürütme izni vermek için üçüncü karakter ' x ' olur.</span><span class="sxs-lookup"><span data-stu-id="9272c-126">The permission field is a 3-character sequence where the first character is 'r' to grant read access, the second character is 'w' to grant write access, and the third character is 'x' to grant execute permission.</span></span>
<span data-ttu-id="9272c-127">Erişim verilmezse, iznin reddedildiğini belirtmek için '-' karakteri kullanılır.</span><span class="sxs-lookup"><span data-stu-id="9272c-127">If access is not granted, the '-' character is used to denote that the permission is denied.</span></span>

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

### <span data-ttu-id="9272c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9272c-128">CommonParameters</span></span>
<span data-ttu-id="9272c-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9272c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9272c-130">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9272c-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9272c-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9272c-131">INPUTS</span></span>

### <span data-ttu-id="9272c-132">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="9272c-132">None</span></span>

## <span data-ttu-id="9272c-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9272c-133">OUTPUTS</span></span>

### <span data-ttu-id="9272c-134">Microsoft. Windowsazde. Commands. Storage. model. ResourceModel. PSPathAccessControlEntry</span><span class="sxs-lookup"><span data-stu-id="9272c-134">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSPathAccessControlEntry</span></span>

## <span data-ttu-id="9272c-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9272c-135">NOTES</span></span>

## <span data-ttu-id="9272c-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9272c-136">RELATED LINKS</span></span>
