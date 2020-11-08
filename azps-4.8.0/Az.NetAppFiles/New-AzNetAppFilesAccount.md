---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesAccount.md
ms.openlocfilehash: 3d23186ce78b2fc97916e029fae8d9db3df1092c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109536"
---
# <span data-ttu-id="29d67-101">New-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="29d67-101">New-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="29d67-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29d67-102">SYNOPSIS</span></span>
<span data-ttu-id="29d67-103">Yeni bir Azure NetApp dosyaları (ANF) oluşturur.</span><span class="sxs-lookup"><span data-stu-id="29d67-103">Creates a new Azure NetApp Files (ANF) account.</span></span>

## <span data-ttu-id="29d67-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="29d67-104">SYNTAX</span></span>

```
New-AzNetAppFilesAccount -ResourceGroupName <String> -Location <String> -Name <String>
 [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29d67-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="29d67-105">DESCRIPTION</span></span>
<span data-ttu-id="29d67-106">**New-AzNetAppFilesAccount** cmdlet 'ı BIR ANF hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="29d67-106">The **New-AzNetAppFilesAccount** cmdlet creates an ANF account.</span></span>

## <span data-ttu-id="29d67-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="29d67-107">EXAMPLES</span></span>

### <span data-ttu-id="29d67-108">Örnek 1: ANF hesabı oluşturma</span><span class="sxs-lookup"><span data-stu-id="29d67-108">Example 1: Create an ANF account</span></span>
```
PS C:\>New-AzNetAppFilesAccount -ResourceGroupName "MyRG" -Name "MyAnfAccount" -l "westus2"

Output:

Location          : westus2
Id                : /subscriptions/mySubs/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount
Name              : MyAnfAccount
Type              : Microsoft.NetApp/netAppAccounts
Tags              :
ProvisioningState : Succeeded
```

<span data-ttu-id="29d67-109">Bu komut, "MyAnfAccount" yeni ANF hesabını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="29d67-109">This command creates the new ANF account "MyAnfAccount".</span></span>

## <span data-ttu-id="29d67-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="29d67-110">PARAMETERS</span></span>

### <span data-ttu-id="29d67-111">-ActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="29d67-111">-ActiveDirectory</span></span>
<span data-ttu-id="29d67-112">Active Directory 'yi temsil eden bir Hashtable dizisi</span><span class="sxs-lookup"><span data-stu-id="29d67-112">A hashtable array which represents the active directories</span></span>

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

### <span data-ttu-id="29d67-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29d67-113">-DefaultProfile</span></span>
<span data-ttu-id="29d67-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="29d67-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29d67-115">-Konum</span><span class="sxs-lookup"><span data-stu-id="29d67-115">-Location</span></span>
<span data-ttu-id="29d67-116">Kaynağın konumu</span><span class="sxs-lookup"><span data-stu-id="29d67-116">The location of the resource</span></span>

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

### <span data-ttu-id="29d67-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="29d67-117">-Name</span></span>
<span data-ttu-id="29d67-118">ANF hesabının adı</span><span class="sxs-lookup"><span data-stu-id="29d67-118">The name of the ANF account</span></span>

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

### <span data-ttu-id="29d67-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29d67-119">-ResourceGroupName</span></span>
<span data-ttu-id="29d67-120">ANF hesabının kaynak grubu</span><span class="sxs-lookup"><span data-stu-id="29d67-120">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="29d67-121">Etiketli</span><span class="sxs-lookup"><span data-stu-id="29d67-121">-Tag</span></span>
<span data-ttu-id="29d67-122">Kaynak etiketlerini temsil eden bir Hashtable</span><span class="sxs-lookup"><span data-stu-id="29d67-122">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="29d67-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="29d67-123">-Confirm</span></span>
<span data-ttu-id="29d67-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="29d67-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29d67-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29d67-125">-WhatIf</span></span>
<span data-ttu-id="29d67-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="29d67-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29d67-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="29d67-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29d67-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29d67-128">CommonParameters</span></span>
<span data-ttu-id="29d67-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="29d67-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29d67-130">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="29d67-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29d67-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="29d67-131">INPUTS</span></span>

### <span data-ttu-id="29d67-132">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="29d67-132">None</span></span>

## <span data-ttu-id="29d67-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="29d67-133">OUTPUTS</span></span>

### <span data-ttu-id="29d67-134">Microsoft. Azure. Commands. NetAppFiles. modeller. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="29d67-134">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="29d67-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="29d67-135">NOTES</span></span>

## <span data-ttu-id="29d67-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="29d67-136">RELATED LINKS</span></span>
