---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesAccount.md
ms.openlocfilehash: 621d4d29d061566e894617d5e918440ba531a041
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267259"
---
# <span data-ttu-id="4c3b1-101">Update-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="4c3b1-101">Update-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="4c3b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c3b1-102">SYNOPSIS</span></span>
<span data-ttu-id="4c3b1-103">Bir Azure NetApp dosyaları (ANF) hesabını sağlanan değiştiricilere göre güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="4c3b1-103">Updates an Azure NetApp Files (ANF) account according to the optional modifiers provided.</span></span>

## <span data-ttu-id="4c3b1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4c3b1-104">SYNTAX</span></span>

### <span data-ttu-id="4c3b1-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4c3b1-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesAccount -ResourceGroupName <String> [-Location <String>] -Name <String>
 [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c3b1-106">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="4c3b1-106">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesAccount -ResourceGroupName <String> [-Location <String>] -Name <String>
 -ResourceId <String> [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c3b1-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4c3b1-107">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesAccount -ResourceGroupName <String> [-Location <String>] -Name <String>
 [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>] -InputObject <PSNetAppFilesAccount> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c3b1-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="4c3b1-108">DESCRIPTION</span></span>
<span data-ttu-id="4c3b1-109">**Update-AzNetAppFilesAccount** cmdlet 'i ANF hesabını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="4c3b1-109">The **Update-AzNetAppFilesAccount** cmdlet modifies an ANF account.</span></span>

## <span data-ttu-id="4c3b1-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4c3b1-110">EXAMPLES</span></span>

### <span data-ttu-id="4c3b1-111">Örnek 1: ANF hesabını güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="4c3b1-111">Example 1 : Updates an ANF account</span></span>
```
PS C:\>Update-AzNetAppFilesAccount -ResourceGroupName "MyRG" -l "westus2" -Name "MyAnfAccount" -Tag @{'Tag1' = 'Value1'}

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount
Name              : MyAnfAccount
Type              : Microsoft.NetApp/netAppAccounts
Tags              : {Tag1}
AccountId         : 9fa2ca6d-1e48-4439-30e3-7de056e44e5a
ActiveDirectories :
ProvisioningState : Succeeded
```

<span data-ttu-id="4c3b1-112">Bu komut, verilen hesapta etiketleri belirtilen hesap üzerinde değiştirerek bir güncelleştirme gerçekleştirir.</span><span class="sxs-lookup"><span data-stu-id="4c3b1-112">This command performs an update on the given account modifying the tags to those provided.</span></span>

## <span data-ttu-id="4c3b1-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4c3b1-113">PARAMETERS</span></span>

### <span data-ttu-id="4c3b1-114">-ActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="4c3b1-114">-ActiveDirectory</span></span>
<span data-ttu-id="4c3b1-115">Active Directory 'yi temsil eden bir Hashtable dizisi</span><span class="sxs-lookup"><span data-stu-id="4c3b1-115">A hashtable array which represents the active directories</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c3b1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c3b1-116">-DefaultProfile</span></span>
<span data-ttu-id="4c3b1-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4c3b1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c3b1-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4c3b1-118">-InputObject</span></span>
<span data-ttu-id="4c3b1-119">Güncelleştirilecek hesap nesnesi</span><span class="sxs-lookup"><span data-stu-id="4c3b1-119">The account object to update</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4c3b1-120">-Konum</span><span class="sxs-lookup"><span data-stu-id="4c3b1-120">-Location</span></span>
<span data-ttu-id="4c3b1-121">Kaynağın konumu</span><span class="sxs-lookup"><span data-stu-id="4c3b1-121">The location of the resource</span></span>

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

### <span data-ttu-id="4c3b1-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="4c3b1-122">-Name</span></span>
<span data-ttu-id="4c3b1-123">ANF hesabının adı</span><span class="sxs-lookup"><span data-stu-id="4c3b1-123">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c3b1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c3b1-124">-ResourceGroupName</span></span>
<span data-ttu-id="4c3b1-125">ANF hesabının kaynak grubu</span><span class="sxs-lookup"><span data-stu-id="4c3b1-125">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="4c3b1-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="4c3b1-126">-ResourceId</span></span>
<span data-ttu-id="4c3b1-127">ANF hesabının kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="4c3b1-127">The resource id of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c3b1-128">Etiketli</span><span class="sxs-lookup"><span data-stu-id="4c3b1-128">-Tag</span></span>
<span data-ttu-id="4c3b1-129">Kaynak etiketlerini temsil eden bir Hashtable</span><span class="sxs-lookup"><span data-stu-id="4c3b1-129">A hashtable which represents resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c3b1-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="4c3b1-130">-Confirm</span></span>
<span data-ttu-id="4c3b1-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4c3b1-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c3b1-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c3b1-132">-WhatIf</span></span>
<span data-ttu-id="4c3b1-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4c3b1-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c3b1-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4c3b1-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c3b1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c3b1-135">CommonParameters</span></span>
<span data-ttu-id="4c3b1-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4c3b1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c3b1-137">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="4c3b1-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c3b1-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4c3b1-138">INPUTS</span></span>

### <span data-ttu-id="4c3b1-139">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="4c3b1-139">None</span></span>

## <span data-ttu-id="4c3b1-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4c3b1-140">OUTPUTS</span></span>

### <span data-ttu-id="4c3b1-141">Microsoft. Azure. Commands. NetAppFiles. modeller. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="4c3b1-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="4c3b1-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4c3b1-142">NOTES</span></span>

## <span data-ttu-id="4c3b1-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4c3b1-143">RELATED LINKS</span></span>
