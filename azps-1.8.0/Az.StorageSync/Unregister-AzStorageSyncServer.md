---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/unregister-Azstoragesyncserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Unregister-AzStorageSyncServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Unregister-AzStorageSyncServer.md
ms.openlocfilehash: 87734d63d28785282ad3285ef8cce0a574ba30e3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753946"
---
# <span data-ttu-id="360e9-101">Unregister-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="360e9-101">Unregister-AzStorageSyncServer</span></span>

## <span data-ttu-id="360e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="360e9-102">SYNOPSIS</span></span>
<span data-ttu-id="360e9-103">Uyarı: sunucunun kaydı silindiğinde, bu sunucudaki tüm sunucu uç noktaları art arda silinir.</span><span class="sxs-lookup"><span data-stu-id="360e9-103">Warning: Unregistering a server will result in cascading deletes of all server endpoints on this server.</span></span> <span data-ttu-id="360e9-104">Bu komut, depolama eşitleme hizmeti olan bir sunucunun kaydını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="360e9-104">This command will unregister a server it's the storage sync service.</span></span>

## <span data-ttu-id="360e9-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="360e9-105">SYNTAX</span></span>

### <span data-ttu-id="360e9-106">Inputobjectparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="360e9-106">InputObjectParameterSet (Default)</span></span>
```
Unregister-AzStorageSyncServer [-InputObject] <PSRegisteredServer> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="360e9-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="360e9-107">ResourceIdParameterSet</span></span>
```
Unregister-AzStorageSyncServer [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="360e9-108">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="360e9-108">StringParameterSet</span></span>
```
Unregister-AzStorageSyncServer [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-ServerId] <Guid> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="360e9-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="360e9-109">DESCRIPTION</span></span>
<span data-ttu-id="360e9-110">Bu komut, bir sunucunun depolama eşitleme hizmetinden kaydını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="360e9-110">This command will unregister a server from the storage sync service.</span></span> <span data-ttu-id="360e9-111">Uyarı: sunucunun kaydı silindiğinde, bu sunucudaki tüm sunucu uç noktaları art arda silinir.</span><span class="sxs-lookup"><span data-stu-id="360e9-111">Warning: Unregistering a server will result in cascading deletes of all server endpoints on this server.</span></span> <span data-ttu-id="360e9-112">Yalnızca bu sunucuda hiçbir yolun artık eşitlenmediğinden emin olduğunuzda çağrılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="360e9-112">It should only be called when you are certain that no path on this server is to be synced anymore.</span></span>

## <span data-ttu-id="360e9-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="360e9-113">EXAMPLES</span></span>

### <span data-ttu-id="360e9-114">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="360e9-114">Example 1</span></span>
```powershell
PS C:\> $RegisteredServer = Get-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
PS C:\> Unregister-AzStorageSyncServer -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -ServerId $RegisteredServer.ServerId
```

<span data-ttu-id="360e9-115">Bu komut sunucunun kaydını, bu sunucudaki tüm sunucu uç noktalarının silinmesini sağlayacaktır.</span><span class="sxs-lookup"><span data-stu-id="360e9-115">This command will unregister the server, causing cascading deletes of all server endpoints on this server.</span></span>

## <span data-ttu-id="360e9-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="360e9-116">PARAMETERS</span></span>

### <span data-ttu-id="360e9-117">-Iş</span><span class="sxs-lookup"><span data-stu-id="360e9-117">-AsJob</span></span>
<span data-ttu-id="360e9-118">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="360e9-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="360e9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="360e9-119">-DefaultProfile</span></span>
<span data-ttu-id="360e9-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="360e9-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="360e9-121">-Force</span><span class="sxs-lookup"><span data-stu-id="360e9-121">-Force</span></span>
<span data-ttu-id="360e9-122">Arz-bu komutun onayını atlamaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="360e9-122">Supply -Force to skip confirmation of this command.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="360e9-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="360e9-123">-InputObject</span></span>
<span data-ttu-id="360e9-124">Normalde ardışık düzen aracılığıyla geçirilen RegisteredServer giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="360e9-124">RegisteredServer Input Object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="360e9-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="360e9-125">-PassThru</span></span>
<span data-ttu-id="360e9-126">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="360e9-126">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="360e9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="360e9-127">-ResourceGroupName</span></span>
<span data-ttu-id="360e9-128">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="360e9-128">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="360e9-129">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="360e9-129">-ResourceId</span></span>
<span data-ttu-id="360e9-130">RegisteredServer kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="360e9-130">RegisteredServer Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="360e9-131">-SunucuKimliği</span><span class="sxs-lookup"><span data-stu-id="360e9-131">-ServerId</span></span>
<span data-ttu-id="360e9-132">RegisteredServer 'in adı.</span><span class="sxs-lookup"><span data-stu-id="360e9-132">Name of the RegisteredServer.</span></span>

```yaml
Type: System.Guid
Parameter Sets: StringParameterSet
Aliases: RegisteredServerName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="360e9-133">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="360e9-133">-StorageSyncServiceName</span></span>
<span data-ttu-id="360e9-134">StorageSyncService adı.</span><span class="sxs-lookup"><span data-stu-id="360e9-134">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="360e9-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="360e9-135">-Confirm</span></span>
<span data-ttu-id="360e9-136">Cmdlet 'i çalıştırmadan önce onay ister.</span><span class="sxs-lookup"><span data-stu-id="360e9-136">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="360e9-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="360e9-137">-WhatIf</span></span>
<span data-ttu-id="360e9-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="360e9-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="360e9-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="360e9-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="360e9-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="360e9-140">CommonParameters</span></span>
<span data-ttu-id="360e9-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="360e9-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="360e9-142">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="360e9-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="360e9-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="360e9-143">INPUTS</span></span>

### <span data-ttu-id="360e9-144">Microsoft. Azure. Commands. Storages, EHD.</span><span class="sxs-lookup"><span data-stu-id="360e9-144">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span></span>

### <span data-ttu-id="360e9-145">System. String</span><span class="sxs-lookup"><span data-stu-id="360e9-145">System.String</span></span>

### <span data-ttu-id="360e9-146">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="360e9-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="360e9-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="360e9-147">OUTPUTS</span></span>

### <span data-ttu-id="360e9-148">System. Object</span><span class="sxs-lookup"><span data-stu-id="360e9-148">System.Object</span></span>
## <span data-ttu-id="360e9-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="360e9-149">NOTES</span></span>

## <span data-ttu-id="360e9-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="360e9-150">RELATED LINKS</span></span>
