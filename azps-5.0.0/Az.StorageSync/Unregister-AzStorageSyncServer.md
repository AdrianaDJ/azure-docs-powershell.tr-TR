---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/unregister-Azstoragesyncserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Unregister-AzStorageSyncServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Unregister-AzStorageSyncServer.md
ms.openlocfilehash: f6de2bf731bc11a4b0ec8b6c894e6d77569ec9ce
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275997"
---
# <span data-ttu-id="16da9-101">Unregister-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="16da9-101">Unregister-AzStorageSyncServer</span></span>

## <span data-ttu-id="16da9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16da9-102">SYNOPSIS</span></span>
<span data-ttu-id="16da9-103">Uyarı: sunucunun kaydı silindiğinde, bu sunucudaki tüm sunucu uç noktaları art arda silinir.</span><span class="sxs-lookup"><span data-stu-id="16da9-103">Warning: Unregistering a server will result in cascading deletes of all server endpoints on this server.</span></span> <span data-ttu-id="16da9-104">Bu komut, bir sunucunun depolama eşitleme hizmetinden kaydını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="16da9-104">This command will unregister a server from it's storage sync service.</span></span>

## <span data-ttu-id="16da9-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="16da9-105">SYNTAX</span></span>

### <span data-ttu-id="16da9-106">StringParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="16da9-106">StringParameterSet (Default)</span></span>
```
Unregister-AzStorageSyncServer [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-ServerId] <Guid> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16da9-107">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="16da9-107">InputObjectParameterSet</span></span>
```
Unregister-AzStorageSyncServer [-InputObject] <PSRegisteredServer> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16da9-108">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="16da9-108">ResourceIdParameterSet</span></span>
```
Unregister-AzStorageSyncServer [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16da9-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="16da9-109">DESCRIPTION</span></span>
<span data-ttu-id="16da9-110">Bu komut, bir sunucunun depolama eşitleme hizmetinden kaydını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="16da9-110">This command will unregister a server from the storage sync service.</span></span> <span data-ttu-id="16da9-111">Uyarı: sunucunun kaydı silindiğinde, bu sunucudaki tüm sunucu uç noktaları art arda silinir.</span><span class="sxs-lookup"><span data-stu-id="16da9-111">Warning: Unregistering a server will result in cascading deletes of all server endpoints on this server.</span></span> <span data-ttu-id="16da9-112">Yalnızca bu sunucuda hiçbir yolun artık eşitlenmediğinden emin olduğunuzda çağrılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="16da9-112">It should only be called when you are certain that no path on this server is to be synced anymore.</span></span>

## <span data-ttu-id="16da9-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="16da9-113">EXAMPLES</span></span>

### <span data-ttu-id="16da9-114">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="16da9-114">Example 1</span></span>
```powershell
PS C:\> $RegisteredServer = Get-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
PS C:\> Unregister-AzStorageSyncServer -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -ServerId $RegisteredServer.ServerId
```

<span data-ttu-id="16da9-115">Bu komut sunucunun kaydını, bu sunucudaki tüm sunucu uç noktalarının silinmesini sağlayacaktır.</span><span class="sxs-lookup"><span data-stu-id="16da9-115">This command will unregister the server, causing cascading deletes of all server endpoints on this server.</span></span>

## <span data-ttu-id="16da9-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="16da9-116">PARAMETERS</span></span>

### <span data-ttu-id="16da9-117">-Iş</span><span class="sxs-lookup"><span data-stu-id="16da9-117">-AsJob</span></span>
<span data-ttu-id="16da9-118">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="16da9-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="16da9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16da9-119">-DefaultProfile</span></span>
<span data-ttu-id="16da9-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="16da9-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16da9-121">-Force</span><span class="sxs-lookup"><span data-stu-id="16da9-121">-Force</span></span>
<span data-ttu-id="16da9-122">Arz-bu komutun onayını atlamaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="16da9-122">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="16da9-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="16da9-123">-InputObject</span></span>
<span data-ttu-id="16da9-124">Normalde ardışık düzen aracılığıyla geçirilen RegisteredServer giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="16da9-124">RegisteredServer Input Object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="16da9-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="16da9-125">-PassThru</span></span>
<span data-ttu-id="16da9-126">Normal yürütmede, bu cmdlet başarı durumunda değer döndürmez.</span><span class="sxs-lookup"><span data-stu-id="16da9-126">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="16da9-127">Geçiş parametresini sağlarsanız, cmdlet başarılı yürütmeden sonra bir ardışık düzene bir değer yazar.</span><span class="sxs-lookup"><span data-stu-id="16da9-127">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="16da9-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16da9-128">-ResourceGroupName</span></span>
<span data-ttu-id="16da9-129">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="16da9-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="16da9-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="16da9-130">-ResourceId</span></span>
<span data-ttu-id="16da9-131">RegisteredServer kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="16da9-131">RegisteredServer Resource Id</span></span>

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

### <span data-ttu-id="16da9-132">-SunucuKimliği</span><span class="sxs-lookup"><span data-stu-id="16da9-132">-ServerId</span></span>
<span data-ttu-id="16da9-133">RegisteredServer 'in adı.</span><span class="sxs-lookup"><span data-stu-id="16da9-133">Name of the RegisteredServer.</span></span>

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

### <span data-ttu-id="16da9-134">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="16da9-134">-StorageSyncServiceName</span></span>
<span data-ttu-id="16da9-135">StorageSyncService adı.</span><span class="sxs-lookup"><span data-stu-id="16da9-135">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="16da9-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="16da9-136">-Confirm</span></span>
<span data-ttu-id="16da9-137">Cmdlet 'i çalıştırmadan önce onay ister.</span><span class="sxs-lookup"><span data-stu-id="16da9-137">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16da9-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16da9-138">-WhatIf</span></span>
<span data-ttu-id="16da9-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="16da9-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="16da9-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="16da9-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16da9-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16da9-141">CommonParameters</span></span>
<span data-ttu-id="16da9-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="16da9-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16da9-143">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16da9-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16da9-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="16da9-144">INPUTS</span></span>

### <span data-ttu-id="16da9-145">Microsoft. Azure. Commands. Storages, EHD.</span><span class="sxs-lookup"><span data-stu-id="16da9-145">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span></span>

### <span data-ttu-id="16da9-146">System. String</span><span class="sxs-lookup"><span data-stu-id="16da9-146">System.String</span></span>

### <span data-ttu-id="16da9-147">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="16da9-147">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="16da9-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="16da9-148">OUTPUTS</span></span>

### <span data-ttu-id="16da9-149">System. Object</span><span class="sxs-lookup"><span data-stu-id="16da9-149">System.Object</span></span>
## <span data-ttu-id="16da9-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="16da9-150">NOTES</span></span>

## <span data-ttu-id="16da9-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="16da9-151">RELATED LINKS</span></span>
