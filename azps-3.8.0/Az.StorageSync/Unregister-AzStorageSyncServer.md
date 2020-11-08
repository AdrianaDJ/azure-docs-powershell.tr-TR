---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/unregister-Azstoragesyncserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Unregister-AzStorageSyncServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Unregister-AzStorageSyncServer.md
ms.openlocfilehash: f6de2bf731bc11a4b0ec8b6c894e6d77569ec9ce
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098649"
---
# <span data-ttu-id="7356c-101">Unregister-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="7356c-101">Unregister-AzStorageSyncServer</span></span>

## <span data-ttu-id="7356c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7356c-102">SYNOPSIS</span></span>
<span data-ttu-id="7356c-103">Uyarı: sunucunun kaydı silindiğinde, bu sunucudaki tüm sunucu uç noktaları art arda silinir.</span><span class="sxs-lookup"><span data-stu-id="7356c-103">Warning: Unregistering a server will result in cascading deletes of all server endpoints on this server.</span></span> <span data-ttu-id="7356c-104">Bu komut, bir sunucunun depolama eşitleme hizmetinden kaydını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7356c-104">This command will unregister a server from it's storage sync service.</span></span>

## <span data-ttu-id="7356c-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7356c-105">SYNTAX</span></span>

### <span data-ttu-id="7356c-106">StringParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7356c-106">StringParameterSet (Default)</span></span>
```
Unregister-AzStorageSyncServer [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-ServerId] <Guid> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7356c-107">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="7356c-107">InputObjectParameterSet</span></span>
```
Unregister-AzStorageSyncServer [-InputObject] <PSRegisteredServer> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7356c-108">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="7356c-108">ResourceIdParameterSet</span></span>
```
Unregister-AzStorageSyncServer [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7356c-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="7356c-109">DESCRIPTION</span></span>
<span data-ttu-id="7356c-110">Bu komut, bir sunucunun depolama eşitleme hizmetinden kaydını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7356c-110">This command will unregister a server from the storage sync service.</span></span> <span data-ttu-id="7356c-111">Uyarı: sunucunun kaydı silindiğinde, bu sunucudaki tüm sunucu uç noktaları art arda silinir.</span><span class="sxs-lookup"><span data-stu-id="7356c-111">Warning: Unregistering a server will result in cascading deletes of all server endpoints on this server.</span></span> <span data-ttu-id="7356c-112">Yalnızca bu sunucuda hiçbir yolun artık eşitlenmediğinden emin olduğunuzda çağrılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="7356c-112">It should only be called when you are certain that no path on this server is to be synced anymore.</span></span>

## <span data-ttu-id="7356c-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7356c-113">EXAMPLES</span></span>

### <span data-ttu-id="7356c-114">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7356c-114">Example 1</span></span>
```powershell
PS C:\> $RegisteredServer = Get-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
PS C:\> Unregister-AzStorageSyncServer -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -ServerId $RegisteredServer.ServerId
```

<span data-ttu-id="7356c-115">Bu komut sunucunun kaydını, bu sunucudaki tüm sunucu uç noktalarının silinmesini sağlayacaktır.</span><span class="sxs-lookup"><span data-stu-id="7356c-115">This command will unregister the server, causing cascading deletes of all server endpoints on this server.</span></span>

## <span data-ttu-id="7356c-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7356c-116">PARAMETERS</span></span>

### <span data-ttu-id="7356c-117">-Iş</span><span class="sxs-lookup"><span data-stu-id="7356c-117">-AsJob</span></span>
<span data-ttu-id="7356c-118">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="7356c-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7356c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7356c-119">-DefaultProfile</span></span>
<span data-ttu-id="7356c-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7356c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7356c-121">-Force</span><span class="sxs-lookup"><span data-stu-id="7356c-121">-Force</span></span>
<span data-ttu-id="7356c-122">Arz-bu komutun onayını atlamaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="7356c-122">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="7356c-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7356c-123">-InputObject</span></span>
<span data-ttu-id="7356c-124">Normalde ardışık düzen aracılığıyla geçirilen RegisteredServer giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="7356c-124">RegisteredServer Input Object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="7356c-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="7356c-125">-PassThru</span></span>
<span data-ttu-id="7356c-126">Normal yürütmede, bu cmdlet başarı durumunda değer döndürmez.</span><span class="sxs-lookup"><span data-stu-id="7356c-126">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="7356c-127">Geçiş parametresini sağlarsanız, cmdlet başarılı yürütmeden sonra bir ardışık düzene bir değer yazar.</span><span class="sxs-lookup"><span data-stu-id="7356c-127">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="7356c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7356c-128">-ResourceGroupName</span></span>
<span data-ttu-id="7356c-129">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="7356c-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="7356c-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="7356c-130">-ResourceId</span></span>
<span data-ttu-id="7356c-131">RegisteredServer kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="7356c-131">RegisteredServer Resource Id</span></span>

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

### <span data-ttu-id="7356c-132">-SunucuKimliği</span><span class="sxs-lookup"><span data-stu-id="7356c-132">-ServerId</span></span>
<span data-ttu-id="7356c-133">RegisteredServer 'in adı.</span><span class="sxs-lookup"><span data-stu-id="7356c-133">Name of the RegisteredServer.</span></span>

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

### <span data-ttu-id="7356c-134">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="7356c-134">-StorageSyncServiceName</span></span>
<span data-ttu-id="7356c-135">StorageSyncService adı.</span><span class="sxs-lookup"><span data-stu-id="7356c-135">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="7356c-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="7356c-136">-Confirm</span></span>
<span data-ttu-id="7356c-137">Cmdlet 'i çalıştırmadan önce onay ister.</span><span class="sxs-lookup"><span data-stu-id="7356c-137">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7356c-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7356c-138">-WhatIf</span></span>
<span data-ttu-id="7356c-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7356c-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7356c-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7356c-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7356c-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7356c-141">CommonParameters</span></span>
<span data-ttu-id="7356c-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7356c-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7356c-143">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7356c-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7356c-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7356c-144">INPUTS</span></span>

### <span data-ttu-id="7356c-145">Microsoft. Azure. Commands. Storages, EHD.</span><span class="sxs-lookup"><span data-stu-id="7356c-145">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span></span>

### <span data-ttu-id="7356c-146">System. String</span><span class="sxs-lookup"><span data-stu-id="7356c-146">System.String</span></span>

### <span data-ttu-id="7356c-147">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7356c-147">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7356c-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7356c-148">OUTPUTS</span></span>

### <span data-ttu-id="7356c-149">System. Object</span><span class="sxs-lookup"><span data-stu-id="7356c-149">System.Object</span></span>
## <span data-ttu-id="7356c-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7356c-150">NOTES</span></span>

## <span data-ttu-id="7356c-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7356c-151">RELATED LINKS</span></span>
