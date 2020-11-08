---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseWorkspace.md
ms.openlocfilehash: fb3613555e65b0d13650e5c15189edd865ab2b89
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109926"
---
# <span data-ttu-id="2a7a3-101">New-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="2a7a3-101">New-AzSynapseWorkspace</span></span>

## <span data-ttu-id="2a7a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a7a3-102">SYNOPSIS</span></span>
<span data-ttu-id="2a7a3-103">SYNAPSE Analytics çalışma alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2a7a3-103">Creates a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="2a7a3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2a7a3-104">SYNTAX</span></span>

```
New-AzSynapseWorkspace -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 -DefaultDataLakeStorageAccountName <String> -DefaultDataLakeStorageFilesystem <String>
 -SqlAdministratorLoginCredential <PSCredential> [-ManagedVirtualNetwork <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a7a3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2a7a3-105">DESCRIPTION</span></span>
<span data-ttu-id="2a7a3-106">**New-AzSynapseWorkspace** cmdlet 'ı bir Azure SYNAPSE Analytics çalışma alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2a7a3-106">The **New-AzSynapseWorkspace** cmdlet creates an Azure Synapse Analytics workspace.</span></span>

## <span data-ttu-id="2a7a3-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2a7a3-107">EXAMPLES</span></span>

### <span data-ttu-id="2a7a3-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2a7a3-108">Example 1</span></span>
```powershell
PS C:\> $password = ConvertTo-SecureString "Password123!" -AsPlainText -Force
PS C:\> $creds = New-Object System.Management.Automation.PSCredential ("ContosoUser", $password)
PS C:\> New-AzSynapseWorkspace -ResourceGroupName ContosoResourceGroup -Name ContosoWorkspace -Location northeurope -DefaultDataLakeStorageAccountName ContosoAdlGen2Storage -DefaultDataLakeStorageFilesystem ContosoFileSystem -SqlAdministratorLoginCredential $creds -AsJob
```

<span data-ttu-id="2a7a3-109">Bu komut, contosoresourcegroup adlı kaynak grubunda contosoadlgenstorage veri deposunu kullanan contoso</span><span class="sxs-lookup"><span data-stu-id="2a7a3-109">This command creates a Synapse Analytics workspace named ContosoWorkspace that uses the ContosoAdlGenStorage Data Store, in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="2a7a3-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2a7a3-110">PARAMETERS</span></span>

### <span data-ttu-id="2a7a3-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="2a7a3-111">-AsJob</span></span>
<span data-ttu-id="2a7a3-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="2a7a3-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2a7a3-113">-DefaultDataLakeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="2a7a3-113">-DefaultDataLakeStorageAccountName</span></span>
<span data-ttu-id="2a7a3-114">Varsayılan ADLS Gen2 depolama hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="2a7a3-114">The default ADLS Gen2 storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a7a3-115">-DefaultDataLakeStorageFilesystem</span><span class="sxs-lookup"><span data-stu-id="2a7a3-115">-DefaultDataLakeStorageFilesystem</span></span>
<span data-ttu-id="2a7a3-116">Varsayılan ADLS Gen2 dosya sistemi.</span><span class="sxs-lookup"><span data-stu-id="2a7a3-116">The default ADLS Gen2 file system.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a7a3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a7a3-117">-DefaultProfile</span></span>
<span data-ttu-id="2a7a3-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2a7a3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a7a3-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="2a7a3-119">-Location</span></span>
<span data-ttu-id="2a7a3-120">Kaynağın oluşturulması gereken Azure bölgesi.</span><span class="sxs-lookup"><span data-stu-id="2a7a3-120">Azure region where the resource should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a7a3-121">-ManagedVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2a7a3-121">-ManagedVirtualNetwork</span></span>
<span data-ttu-id="2a7a3-122">Azure SYNAPSE çalışma alanı için adanmış bir Synapse yönetimli sanal ağın adı.</span><span class="sxs-lookup"><span data-stu-id="2a7a3-122">Name of a Synapse-managed virtual network dedicated for the Azure Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: default

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a7a3-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="2a7a3-123">-Name</span></span>
<span data-ttu-id="2a7a3-124">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="2a7a3-124">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a7a3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a7a3-125">-ResourceGroupName</span></span>
<span data-ttu-id="2a7a3-126">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="2a7a3-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a7a3-127">-SqlAdministratorLoginCredential</span><span class="sxs-lookup"><span data-stu-id="2a7a3-127">-SqlAdministratorLoginCredential</span></span>
<span data-ttu-id="2a7a3-128">SQL Yöneticisi kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="2a7a3-128">SQL administrator credentials.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a7a3-129">Etiketli</span><span class="sxs-lookup"><span data-stu-id="2a7a3-129">-Tag</span></span>
<span data-ttu-id="2a7a3-130">Kaynakla ilişkili etiketlerin dize sözlüğü.</span><span class="sxs-lookup"><span data-stu-id="2a7a3-130">A string,string dictionary of tags associated with the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a7a3-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="2a7a3-131">-Confirm</span></span>
<span data-ttu-id="2a7a3-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2a7a3-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a7a3-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a7a3-133">-WhatIf</span></span>
<span data-ttu-id="2a7a3-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2a7a3-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a7a3-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2a7a3-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a7a3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a7a3-136">CommonParameters</span></span>
<span data-ttu-id="2a7a3-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2a7a3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a7a3-138">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="2a7a3-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a7a3-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2a7a3-139">INPUTS</span></span>

### <span data-ttu-id="2a7a3-140">System. String</span><span class="sxs-lookup"><span data-stu-id="2a7a3-140">System.String</span></span>

### <span data-ttu-id="2a7a3-141">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="2a7a3-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="2a7a3-142">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="2a7a3-142">System.Management.Automation.PSCredential</span></span>

## <span data-ttu-id="2a7a3-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2a7a3-143">OUTPUTS</span></span>

### <span data-ttu-id="2a7a3-144">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="2a7a3-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="2a7a3-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2a7a3-145">NOTES</span></span>

## <span data-ttu-id="2a7a3-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2a7a3-146">RELATED LINKS</span></span>
