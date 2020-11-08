---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeShare.md
ms.openlocfilehash: 12ab6c1948f0864c7dcb930d0a658088fd83262c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275168"
---
# <span data-ttu-id="5dbf1-101">New-AzStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="5dbf1-101">New-AzStackEdgeShare</span></span>

## <span data-ttu-id="5dbf1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5dbf1-102">SYNOPSIS</span></span>
<span data-ttu-id="5dbf1-103">Cihazda yeni bir paylaşım oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5dbf1-103">Creates a new share on the device.</span></span>

## <span data-ttu-id="5dbf1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5dbf1-104">SYNTAX</span></span>

### <span data-ttu-id="5dbf1-105">SmbParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5dbf1-105">SmbParameterSet (Default)</span></span>
```
New-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-SMB]
 [-UserAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5dbf1-106">CloudShareNfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="5dbf1-106">CloudShareNfsParameterSet</span></span>
```
New-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StorageAccountCredentialName] <String> [-CloudShare] -DataFormat <String> [-ContainerName <String>] [-NFS]
 [-ClientAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5dbf1-107">CloudShareSmbParameterSet</span><span class="sxs-lookup"><span data-stu-id="5dbf1-107">CloudShareSmbParameterSet</span></span>
```
New-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StorageAccountCredentialName] <String> [-CloudShare] -DataFormat <String> [-ContainerName <String>] [-SMB]
 [-UserAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5dbf1-108">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="5dbf1-108">NfsParameterSet</span></span>
```
New-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-NFS]
 [-ClientAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5dbf1-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="5dbf1-109">DESCRIPTION</span></span>
<span data-ttu-id="5dbf1-110">**New-Azstackedgesshare** cmdlet 'ı, yığın uç cihazında yeni bir paylaşım oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5dbf1-110">The **New-AzStackEdgeShare** cmdlet creates a new share on the Stack Edge device.</span></span>

## <span data-ttu-id="5dbf1-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5dbf1-111">EXAMPLES</span></span>

### <span data-ttu-id="5dbf1-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5dbf1-112">Example 1</span></span>
```
PS C:\> New-AzStackEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name share-1 -SMB
-StorageAccountCredentialName storageCredentialName -DataFormat PageBlob
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-1    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
```

## <span data-ttu-id="5dbf1-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5dbf1-113">PARAMETERS</span></span>

### <span data-ttu-id="5dbf1-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="5dbf1-114">-AsJob</span></span>
<span data-ttu-id="5dbf1-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="5dbf1-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5dbf1-116">-Clientacerişimrıght</span><span class="sxs-lookup"><span data-stu-id="5dbf1-116">-ClientAccessRight</span></span>
<span data-ttu-id="5dbf1-117">ClientIds için okuma/yazma erişimi, Ex: @ (@ {"Clıtıd" = "192.168.10.10"; " AccessRight "=" NoAccess "}, @ {" Clıen"=" 192.168.10.11 ";" AccessRight "=" ReadOnly "})</span><span class="sxs-lookup"><span data-stu-id="5dbf1-117">Read/Write Access for clientIds, For ex:@(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: CloudShareNfsParameterSet, NfsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dbf1-118">-CloudShare</span><span class="sxs-lookup"><span data-stu-id="5dbf1-118">-CloudShare</span></span>
<span data-ttu-id="5dbf1-119">Var olan StorageAccountCredential 'in kaynak adını sağlayın</span><span class="sxs-lookup"><span data-stu-id="5dbf1-119">Provide existing StorageAccountCredential's Resource Name</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CloudShareNfsParameterSet, CloudShareSmbParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dbf1-120">-Kapsayıcıadı</span><span class="sxs-lookup"><span data-stu-id="5dbf1-120">-ContainerName</span></span>
<span data-ttu-id="5dbf1-121">Kapsayıcı adı (belirtilen veri biçimine bağlı olarak, bu ad, Azure dosyalarının/Pageblob/blok blob 'un adını temsil eder)</span><span class="sxs-lookup"><span data-stu-id="5dbf1-121">Container name (Based on the data format specified, this represents the name of Azure Files/Pageblob/Block blob)</span></span>

```yaml
Type: System.String
Parameter Sets: CloudShareNfsParameterSet, CloudShareSmbParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dbf1-122">-DataFormat</span><span class="sxs-lookup"><span data-stu-id="5dbf1-122">-DataFormat</span></span>
<span data-ttu-id="5dbf1-123">Veri biçimini ayarla Ex: PageBlob, BlobBlob</span><span class="sxs-lookup"><span data-stu-id="5dbf1-123">Set Data Format ex: PageBlob, BlobBlob</span></span>

```yaml
Type: System.String
Parameter Sets: CloudShareNfsParameterSet, CloudShareSmbParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dbf1-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5dbf1-124">-DefaultProfile</span></span>
<span data-ttu-id="5dbf1-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5dbf1-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5dbf1-126">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="5dbf1-126">-DeviceName</span></span>
<span data-ttu-id="5dbf1-127">Cihaz adı</span><span class="sxs-lookup"><span data-stu-id="5dbf1-127">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5dbf1-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="5dbf1-128">-Name</span></span>
<span data-ttu-id="5dbf1-129">Kaynak adı</span><span class="sxs-lookup"><span data-stu-id="5dbf1-129">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EdgeShareName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5dbf1-130">-NFS</span><span class="sxs-lookup"><span data-stu-id="5dbf1-130">-NFS</span></span>
<span data-ttu-id="5dbf1-131">Paylaşım oluşturmak için AccessProtocol</span><span class="sxs-lookup"><span data-stu-id="5dbf1-131">AccessProtocol in the case of creating Share</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CloudShareNfsParameterSet, NfsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dbf1-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5dbf1-132">-ResourceGroupName</span></span>
<span data-ttu-id="5dbf1-133">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="5dbf1-133">Resource Group Name</span></span>

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

### <span data-ttu-id="5dbf1-134">-SMB</span><span class="sxs-lookup"><span data-stu-id="5dbf1-134">-SMB</span></span>
<span data-ttu-id="5dbf1-135">Paylaşım oluşturmak için AccessProtocol</span><span class="sxs-lookup"><span data-stu-id="5dbf1-135">AccessProtocol in the case of creating Share</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SmbParameterSet, CloudShareSmbParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dbf1-136">-StorageAccountCredentialName</span><span class="sxs-lookup"><span data-stu-id="5dbf1-136">-StorageAccountCredentialName</span></span>
<span data-ttu-id="5dbf1-137">Var olan StorageAccountCredential 'in kaynak adını sağlayın</span><span class="sxs-lookup"><span data-stu-id="5dbf1-137">Provide existing StorageAccountCredential's Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: CloudShareNfsParameterSet, CloudShareSmbParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5dbf1-138">-UserAccessRight</span><span class="sxs-lookup"><span data-stu-id="5dbf1-138">-UserAccessRight</span></span>
<span data-ttu-id="5dbf1-139">SMB paylaşım türlerine erişim sağlamak için, Ex: @ (@ {"kullanıcıadı" = "Kullanıcı-adı-1"; " AccessRight "=" Read "}, @ {" kullanıcıadı "=" Kullanıcı-adı-2 ";" AccessRight "=" Read "}, @ {" kullanıcıadı "=" Kullanıcı-adı-3 ";" AccessRight "=" özel "})</span><span class="sxs-lookup"><span data-stu-id="5dbf1-139">provide access right along with existing usernames to access SMB Share types, For ex: @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: SmbParameterSet, CloudShareSmbParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dbf1-140">-Onay</span><span class="sxs-lookup"><span data-stu-id="5dbf1-140">-Confirm</span></span>
<span data-ttu-id="5dbf1-141">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5dbf1-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5dbf1-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5dbf1-142">-WhatIf</span></span>
<span data-ttu-id="5dbf1-143">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5dbf1-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5dbf1-144">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5dbf1-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5dbf1-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5dbf1-145">CommonParameters</span></span>
<span data-ttu-id="5dbf1-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5dbf1-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5dbf1-147">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5dbf1-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5dbf1-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5dbf1-148">INPUTS</span></span>

### <span data-ttu-id="5dbf1-149">System. String</span><span class="sxs-lookup"><span data-stu-id="5dbf1-149">System.String</span></span>

## <span data-ttu-id="5dbf1-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5dbf1-150">OUTPUTS</span></span>

### <span data-ttu-id="5dbf1-151">Microsoft. Azure. PowerShell. cmdlet. yığın</span><span class="sxs-lookup"><span data-stu-id="5dbf1-151">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span></span>

## <span data-ttu-id="5dbf1-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5dbf1-152">NOTES</span></span>

## <span data-ttu-id="5dbf1-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5dbf1-153">RELATED LINKS</span></span>
