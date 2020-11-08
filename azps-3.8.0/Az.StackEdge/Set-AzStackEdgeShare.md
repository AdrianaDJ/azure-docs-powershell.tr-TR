---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/set-azstackedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeShare.md
ms.openlocfilehash: 2b6c5d5f2295398975d912521ff6d0f001bbd3a2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94103895"
---
# <span data-ttu-id="464c6-101">Set-AzStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="464c6-101">Set-AzStackEdgeShare</span></span>

## <span data-ttu-id="464c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="464c6-102">SYNOPSIS</span></span>
<span data-ttu-id="464c6-103">Aygıtın paylaşımını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="464c6-103">Updates the share for a device.</span></span>

## <span data-ttu-id="464c6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="464c6-104">SYNTAX</span></span>

### <span data-ttu-id="464c6-105">SmbParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="464c6-105">SmbParameterSet (Default)</span></span>
```
Set-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -UserAccessRight <Hashtable[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="464c6-106">Updatebyresourceıdsmbparameterset</span><span class="sxs-lookup"><span data-stu-id="464c6-106">UpdateByResourceIdSmbParameterSet</span></span>
```
Set-AzStackEdgeShare -ResourceId <String> -UserAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="464c6-107">UpdateByResourceIdNfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="464c6-107">UpdateByResourceIdNfsParameterSet</span></span>
```
Set-AzStackEdgeShare -ResourceId <String> -ClientAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="464c6-108">UpdateByInputObjectSmbParameterSet</span><span class="sxs-lookup"><span data-stu-id="464c6-108">UpdateByInputObjectSmbParameterSet</span></span>
```
Set-AzStackEdgeShare -InputObject <PSStackEdgeShare> -UserAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="464c6-109">UpdateByInputObjectNfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="464c6-109">UpdateByInputObjectNfsParameterSet</span></span>
```
Set-AzStackEdgeShare -InputObject <PSStackEdgeShare> -ClientAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="464c6-110">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="464c6-110">NfsParameterSet</span></span>
```
Set-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -ClientAccessRight <Hashtable[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="464c6-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="464c6-111">DESCRIPTION</span></span>
<span data-ttu-id="464c6-112">Bu **set-Azstackedges,** erişim haklarını değiştirecek</span><span class="sxs-lookup"><span data-stu-id="464c6-112">This **Set-AzStackEdgeShare** will replace the access rights</span></span>

## <span data-ttu-id="464c6-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="464c6-113">EXAMPLES</span></span>

### <span data-ttu-id="464c6-114">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="464c6-114">Example 1</span></span>
```powershell
PS C:\> $AccessRights = @(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})
PS C:\> Set-AzStackEdgeShare -ResourceGroupName resource-group-name -ClientAccessRight $AccessRights
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-2    NFS        Cloud            PageBlob         resource-group-name   storage-account-name
## $ClientAccessRights = @(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})
## Possible values for AccessRight options are 'NoAccess', 'ReadOnly', 'ReadWrite'
```

### <span data-ttu-id="464c6-115">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="464c6-115">Example 2</span></span>
```powershell
PS C:\> $AccessRights = @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})
PS C:\> Set-AzStackEdgeShare -ResourceGroupName resource-group-name -UserAccessRight $AccessRights
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-1    SMB        Cloud            PageBlob         resource-group-name   storage-account-name
## $UserAccessRights = @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})
## Possible values for AccessRight are 'Change', 'Read', 'Custom'
```

## <span data-ttu-id="464c6-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="464c6-116">PARAMETERS</span></span>

### <span data-ttu-id="464c6-117">-Iş</span><span class="sxs-lookup"><span data-stu-id="464c6-117">-AsJob</span></span>
<span data-ttu-id="464c6-118">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="464c6-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="464c6-119">-Clientacerişimrıght</span><span class="sxs-lookup"><span data-stu-id="464c6-119">-ClientAccessRight</span></span>
<span data-ttu-id="464c6-120">ClientIds için okuma/yazma erişimi, Ex: @ (@ {"Clıtıd" = "192.168.10.10"; " AccessRight "=" NoAccess "}, @ {" Clıen"=" 192.168.10.11 ";" AccessRight "=" ReadOnly "})</span><span class="sxs-lookup"><span data-stu-id="464c6-120">Read/Write Access for clientIds, For ex:@(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: UpdateByResourceIdNfsParameterSet, UpdateByInputObjectNfsParameterSet, NfsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="464c6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="464c6-121">-DefaultProfile</span></span>
<span data-ttu-id="464c6-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="464c6-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="464c6-123">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="464c6-123">-DeviceName</span></span>
<span data-ttu-id="464c6-124">Cihaz adı</span><span class="sxs-lookup"><span data-stu-id="464c6-124">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: SmbParameterSet, NfsParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="464c6-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="464c6-125">-InputObject</span></span>
<span data-ttu-id="464c6-126">Giriş nesnesi</span><span class="sxs-lookup"><span data-stu-id="464c6-126">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare
Parameter Sets: UpdateByInputObjectSmbParameterSet, UpdateByInputObjectNfsParameterSet
Aliases: EdgeShare

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="464c6-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="464c6-127">-Name</span></span>
<span data-ttu-id="464c6-128">Kaynak adı</span><span class="sxs-lookup"><span data-stu-id="464c6-128">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: SmbParameterSet, NfsParameterSet
Aliases: EdgeShareName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="464c6-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="464c6-129">-ResourceGroupName</span></span>
<span data-ttu-id="464c6-130">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="464c6-130">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SmbParameterSet, NfsParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="464c6-131">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="464c6-131">-ResourceId</span></span>
<span data-ttu-id="464c6-132">Azure RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="464c6-132">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdSmbParameterSet, UpdateByResourceIdNfsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="464c6-133">-UserAccessRight</span><span class="sxs-lookup"><span data-stu-id="464c6-133">-UserAccessRight</span></span>
<span data-ttu-id="464c6-134">SMB paylaşım türlerine erişim sağlamak için, Ex: @ (@ {"kullanıcıadı" = "Kullanıcı-adı-1"; " AccessRight "=" Read "}, @ {" kullanıcıadı "=" Kullanıcı-adı-2 ";" AccessRight "=" Read "}, @ {" kullanıcıadı "=" Kullanıcı-adı-3 ";" AccessRight "=" özel "})</span><span class="sxs-lookup"><span data-stu-id="464c6-134">provide access right along with existing usernames to access SMB Share types, For ex: @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: SmbParameterSet, UpdateByResourceIdSmbParameterSet, UpdateByInputObjectSmbParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="464c6-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="464c6-135">-Confirm</span></span>
<span data-ttu-id="464c6-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="464c6-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="464c6-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="464c6-137">-WhatIf</span></span>
<span data-ttu-id="464c6-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="464c6-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="464c6-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="464c6-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="464c6-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="464c6-140">CommonParameters</span></span>
<span data-ttu-id="464c6-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="464c6-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="464c6-142">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="464c6-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="464c6-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="464c6-143">INPUTS</span></span>

### <span data-ttu-id="464c6-144">System. String</span><span class="sxs-lookup"><span data-stu-id="464c6-144">System.String</span></span>

### <span data-ttu-id="464c6-145">Microsoft. Azure. PowerShell. cmdlet. yığın</span><span class="sxs-lookup"><span data-stu-id="464c6-145">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span></span>

## <span data-ttu-id="464c6-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="464c6-146">OUTPUTS</span></span>

### <span data-ttu-id="464c6-147">Microsoft. Azure. PowerShell. cmdlet. yığın</span><span class="sxs-lookup"><span data-stu-id="464c6-147">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span></span>

## <span data-ttu-id="464c6-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="464c6-148">NOTES</span></span>

## <span data-ttu-id="464c6-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="464c6-149">RELATED LINKS</span></span>
