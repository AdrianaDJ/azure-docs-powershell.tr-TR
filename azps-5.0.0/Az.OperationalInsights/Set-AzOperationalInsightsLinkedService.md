---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightslinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsLinkedService.md
ms.openlocfilehash: 3535cc8956643351a6637134cc7dcdd805ed80c3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278078"
---
# <span data-ttu-id="598ef-101">Set-AzOperationalInsightsLinkedService</span><span class="sxs-lookup"><span data-stu-id="598ef-101">Set-AzOperationalInsightsLinkedService</span></span>

## <span data-ttu-id="598ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="598ef-102">SYNOPSIS</span></span>
<span data-ttu-id="598ef-103">çalışma alanı için bağlantı hizmeti</span><span class="sxs-lookup"><span data-stu-id="598ef-103">link service for workspace</span></span>

## <span data-ttu-id="598ef-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="598ef-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsLinkedService [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-LinkedServiceName] <String> [-Tags <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-WriteAccessResourceId <String>] [-ResourceId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="598ef-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="598ef-105">DESCRIPTION</span></span>
<span data-ttu-id="598ef-106">çalışma alanı için bağlantı hizmeti</span><span class="sxs-lookup"><span data-stu-id="598ef-106">link service for workspace</span></span>

## <span data-ttu-id="598ef-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="598ef-107">EXAMPLES</span></span>

### <span data-ttu-id="598ef-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="598ef-108">Example 1</span></span>
```powershell
Set-AzOperationalInsightsLinkedService -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -LinkedServiceName cluster -WriteAccessResourceId /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/clusters/{cluster-name}

Id                    : /subscriptions/{subscription}/resourcegroups/{rg-name}/providers/microsoft.operationalinsights/workspaces/{workspace-name}/linkedservices/cluster
Name                  : {cluster-name}/Cluster
Type                  : Microsoft.OperationalInsights/workspaces/linkedServices
ResourceId            :
WriteAccessResourceId : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/clusters/{cluster-name}
ProvisioningState     : ProvisioningAccount
Tags                  :
```

<span data-ttu-id="598ef-109">çalışma alanı için küme bağlantısı</span><span class="sxs-lookup"><span data-stu-id="598ef-109">link cluster for workspace</span></span>

## <span data-ttu-id="598ef-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="598ef-110">PARAMETERS</span></span>

### <span data-ttu-id="598ef-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="598ef-111">-AsJob</span></span>
<span data-ttu-id="598ef-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="598ef-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="598ef-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="598ef-113">-DefaultProfile</span></span>
<span data-ttu-id="598ef-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="598ef-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="598ef-115">-Linkedhizmetadı</span><span class="sxs-lookup"><span data-stu-id="598ef-115">-LinkedServiceName</span></span>
<span data-ttu-id="598ef-116">Çalışma alanı adı.</span><span class="sxs-lookup"><span data-stu-id="598ef-116">The Workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="598ef-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="598ef-117">-ResourceGroupName</span></span>
<span data-ttu-id="598ef-118">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="598ef-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="598ef-119">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="598ef-119">-ResourceId</span></span>
<span data-ttu-id="598ef-120">Çalışma alanına bağlanacak kaynağın kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="598ef-120">The resource id of the resource that will be linked to the workspace.</span></span>
<span data-ttu-id="598ef-121">Bu, okuma erişimi gerektiren kaynakları bağlamak için kullanılmalıdır</span><span class="sxs-lookup"><span data-stu-id="598ef-121">This should be used for linking resources which require read access</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="598ef-122">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="598ef-122">-Tags</span></span>
<span data-ttu-id="598ef-123">Akıllı.</span><span class="sxs-lookup"><span data-stu-id="598ef-123">Tags.</span></span>

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="598ef-124">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="598ef-124">-WorkspaceName</span></span>
<span data-ttu-id="598ef-125">Çalışma alanı adı.</span><span class="sxs-lookup"><span data-stu-id="598ef-125">The Workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="598ef-126">-Writeaccessresourceıd</span><span class="sxs-lookup"><span data-stu-id="598ef-126">-WriteAccessResourceId</span></span>
<span data-ttu-id="598ef-127">Çalışma alanına bağlanacak kaynağın kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="598ef-127">The resource id of the resource that will be linked to the workspace.</span></span>
<span data-ttu-id="598ef-128">Bu, yazma erişimi gerektiren kaynakları bağlamak için kullanılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="598ef-128">This should be used for linking resources which require write access.</span></span>
<span data-ttu-id="598ef-129">Kümenin sağlama durumu "başarılı" ve geçerli tuş Kasası özellikleri olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="598ef-129">Cluster must have provisioning state "Succeeded" and valid keyvault properties.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="598ef-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="598ef-130">-Confirm</span></span>
<span data-ttu-id="598ef-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="598ef-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="598ef-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="598ef-132">-WhatIf</span></span>
<span data-ttu-id="598ef-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="598ef-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="598ef-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="598ef-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="598ef-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="598ef-135">CommonParameters</span></span>
<span data-ttu-id="598ef-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="598ef-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="598ef-137">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="598ef-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="598ef-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="598ef-138">INPUTS</span></span>

### <span data-ttu-id="598ef-139">System. String</span><span class="sxs-lookup"><span data-stu-id="598ef-139">System.String</span></span>

## <span data-ttu-id="598ef-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="598ef-140">OUTPUTS</span></span>

### <span data-ttu-id="598ef-141">Microsoft. Azure. Commands. Operationalınsights. model. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="598ef-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span></span>

## <span data-ttu-id="598ef-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="598ef-142">NOTES</span></span>

## <span data-ttu-id="598ef-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="598ef-143">RELATED LINKS</span></span>
