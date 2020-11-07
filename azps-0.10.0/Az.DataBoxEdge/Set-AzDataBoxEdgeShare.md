---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/set-azdataboxedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeShare.md
ms.openlocfilehash: ac4f7814898bcbfcee75c4a31273dfbcb6be7335
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935924"
---
# <span data-ttu-id="22158-101">Set-AzDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="22158-101">Set-AzDataBoxEdgeShare</span></span>

## <span data-ttu-id="22158-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22158-102">SYNOPSIS</span></span>
<span data-ttu-id="22158-103">Aygıtın paylaşımını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="22158-103">Updates the share for a device.</span></span>

## <span data-ttu-id="22158-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="22158-104">SYNTAX</span></span>

### <span data-ttu-id="22158-105">SmbParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="22158-105">SmbParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -UserAccessRight <Hashtable[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="22158-106">Updatebyresourceıdsmbparameterset</span><span class="sxs-lookup"><span data-stu-id="22158-106">UpdateByResourceIdSmbParameterSet</span></span>
```
Set-AzDataBoxEdgeShare -ResourceId <String> -UserAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22158-107">UpdateByResourceIdNfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="22158-107">UpdateByResourceIdNfsParameterSet</span></span>
```
Set-AzDataBoxEdgeShare -ResourceId <String> -ClientAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22158-108">UpdateByInputObjectSmbParameterSet</span><span class="sxs-lookup"><span data-stu-id="22158-108">UpdateByInputObjectSmbParameterSet</span></span>
```
Set-AzDataBoxEdgeShare -InputObject <PSDataBoxEdgeShare> -UserAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22158-109">UpdateByInputObjectNfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="22158-109">UpdateByInputObjectNfsParameterSet</span></span>
```
Set-AzDataBoxEdgeShare -InputObject <PSDataBoxEdgeShare> -ClientAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22158-110">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="22158-110">NfsParameterSet</span></span>
```
Set-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -ClientAccessRight <Hashtable[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="22158-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="22158-111">DESCRIPTION</span></span>
<span data-ttu-id="22158-112">Bu **set-Azdataboxedges,** Access haklarını değiştirecek</span><span class="sxs-lookup"><span data-stu-id="22158-112">This **Set-AzDataBoxEdgeShare** will replace the access rights</span></span>

## <span data-ttu-id="22158-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="22158-113">EXAMPLES</span></span>

### <span data-ttu-id="22158-114">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="22158-114">Example 1</span></span>
```powershell
PS C:\> $AccessRights = @(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})
PS C:\> Set-AzDataBoxEdgeShare -ResourceGroupName resource-group-name -ClientAccessRight $AccessRights
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-2    NFS        Cloud            PageBlob         resource-group-name   storage-account-name
## $ClientAccessRights = @(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})
## Possible values for AccessRight options are 'NoAccess', 'ReadOnly', 'ReadWrite'
```

### <span data-ttu-id="22158-115">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="22158-115">Example 2</span></span>
```powershell
PS C:\> $AccessRights = @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})
PS C:\> Set-AzDataBoxEdgeShare -ResourceGroupName resource-group-name -UserAccessRight $AccessRights
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-1    SMB        Cloud            PageBlob         resource-group-name   storage-account-name
## $UserAccessRights = @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})
## Possible values for AccessRight are 'Change', 'Read', 'Custom'
```

## <span data-ttu-id="22158-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="22158-116">PARAMETERS</span></span>

### <span data-ttu-id="22158-117">-Iş</span><span class="sxs-lookup"><span data-stu-id="22158-117">-AsJob</span></span>
<span data-ttu-id="22158-118">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="22158-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="22158-119">-Clientacerişimrıght</span><span class="sxs-lookup"><span data-stu-id="22158-119">-ClientAccessRight</span></span>
<span data-ttu-id="22158-120">ClientIds için okuma/yazma erişimi, Ex: @ (@ {"Clıtıd" = "192.168.10.10"; " AccessRight "=" NoAccess "}, @ {" Clıen"=" 192.168.10.11 ";" AccessRight "=" ReadOnly "})</span><span class="sxs-lookup"><span data-stu-id="22158-120">Read/Write Access for clientIds, For ex:@(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})</span></span>

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

### <span data-ttu-id="22158-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22158-121">-DefaultProfile</span></span>
<span data-ttu-id="22158-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="22158-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22158-123">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="22158-123">-DeviceName</span></span>
<span data-ttu-id="22158-124">Cihaz adı</span><span class="sxs-lookup"><span data-stu-id="22158-124">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: SmbParameterSet, NfsParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22158-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="22158-125">-InputObject</span></span>
<span data-ttu-id="22158-126">Giriş nesnesi</span><span class="sxs-lookup"><span data-stu-id="22158-126">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare
Parameter Sets: UpdateByInputObjectSmbParameterSet, UpdateByInputObjectNfsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="22158-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="22158-127">-Name</span></span>
<span data-ttu-id="22158-128">Kaynak adı</span><span class="sxs-lookup"><span data-stu-id="22158-128">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: SmbParameterSet, NfsParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22158-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22158-129">-ResourceGroupName</span></span>
<span data-ttu-id="22158-130">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="22158-130">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SmbParameterSet, NfsParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22158-131">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="22158-131">-ResourceId</span></span>
<span data-ttu-id="22158-132">Azure RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="22158-132">Azure ResourceId</span></span>

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

### <span data-ttu-id="22158-133">-UserAccessRight</span><span class="sxs-lookup"><span data-stu-id="22158-133">-UserAccessRight</span></span>
<span data-ttu-id="22158-134">SMB paylaşım türlerine erişim sağlamak için, Ex: @ (@ {"kullanıcıadı" = "Kullanıcı-adı-1"; " AccessRight "=" Read "}, @ {" kullanıcıadı "=" Kullanıcı-adı-2 ";" AccessRight "=" Read "}, @ {" kullanıcıadı "=" Kullanıcı-adı-3 ";" AccessRight "=" özel "})</span><span class="sxs-lookup"><span data-stu-id="22158-134">provide access right along with existing usernames to access SMB Share types, For ex: @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})</span></span>

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

### <span data-ttu-id="22158-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="22158-135">-Confirm</span></span>
<span data-ttu-id="22158-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="22158-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22158-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22158-137">-WhatIf</span></span>
<span data-ttu-id="22158-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="22158-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="22158-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="22158-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22158-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22158-140">CommonParameters</span></span>
<span data-ttu-id="22158-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="22158-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22158-142">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="22158-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22158-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="22158-143">INPUTS</span></span>

### <span data-ttu-id="22158-144">System. String</span><span class="sxs-lookup"><span data-stu-id="22158-144">System.String</span></span>

### <span data-ttu-id="22158-145">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDAtaboxedges,</span><span class="sxs-lookup"><span data-stu-id="22158-145">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span></span>

## <span data-ttu-id="22158-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="22158-146">OUTPUTS</span></span>

### <span data-ttu-id="22158-147">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDAtaboxedges,</span><span class="sxs-lookup"><span data-stu-id="22158-147">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span></span>

## <span data-ttu-id="22158-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="22158-148">NOTES</span></span>

## <span data-ttu-id="22158-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="22158-149">RELATED LINKS</span></span>
